# Repository Setup Guide

This guide helps new contributors get started with the WTF CTF writeup repository.

## Quick Start

1. **Fork the repository** on GitHub
2. **Clone your fork**:
   ```bash
   git clone https://github.com/your-username/WTF.git
   cd WTF
   ```

3. **Create a new writeup**:
   ```bash
   # Copy the template
   cp WRITEUP_TEMPLATE.md Web/my-challenge.md
   
   # Edit the writeup
   nano Web/my-challenge.md
   ```

4. **Submit your contribution**:
   ```bash
   git add .
   git commit -m "Add writeup for My Challenge"
   git push origin main
   ```

5. **Create a pull request** on GitHub

## Directory Structure

```
WTF/
├── Web/                    # Web security challenges
├── Crypto/                 # Cryptography challenges
├── Reverse/                # Reverse engineering
├── PWN/                    # Binary exploitation
├── Forensics/              # Digital forensics
├── OSINT/                  # Open source intelligence
├── Misc/                   # Miscellaneous challenges
├── Steganography/          # Steganography challenges
├── WRITEUP_TEMPLATE.md     # Template for new writeups
├── CONTRIBUTING.md         # Detailed contribution guidelines
├── SETUP.md               # This file
└── README.md              # Main repository documentation
```

## Writing Your First Writeup

1. **Choose the right category** for your challenge
2. **Use the template** (`WRITEUP_TEMPLATE.md`) as a starting point
3. **Be detailed** in your explanation
4. **Include code** and commands you used
5. **Add screenshots** when helpful
6. **Test your writeup** by having someone else follow it

## Tools and Environment

### Recommended Tools
- **Web**: Burp Suite, OWASP ZAP, curl
- **Crypto**: Python, SageMath, online cipher tools
- **Reverse**: Ghidra, radare2, GDB
- **PWN**: pwntools, GDB with pwndbg
- **Forensics**: Autopsy, Volatility, Wireshark
- **OSINT**: Google dorking, Shodan, social media tools
- **Steganography**: StegSolve, zsteg, Audacity

### Development Environment
- Git for version control
- Markdown editor (VSCode, Typora, etc.)
- Python for scripting
- Docker for consistent environments (optional)

## Getting Help

- **Read** the CONTRIBUTING.md file for detailed guidelines
- **Check** existing writeups for examples
- **Ask questions** by opening an issue
- **Join discussions** in the GitHub Discussions tab

## Best Practices

- **Security First**: Never include real credentials or attack live systems
- **Educational Focus**: Explain concepts for learning
- **Clean Code**: Format code properly and comment well
- **Reproducible**: Others should be able to follow your steps
- **Respectful**: Follow responsible disclosure practices

---

Happy contributing! 🚩