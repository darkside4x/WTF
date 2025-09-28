# Contributing to WTF - What The Flag

Thank you for your interest in contributing to our CTF writeup repository! This document provides guidelines for contributing high-quality writeups.

## Before You Start

1. **Check for duplicates**: Ensure the challenge hasn't already been documented
2. **Verify completion**: Only submit writeups for challenges you've successfully solved
3. **Respect rules**: Follow the original CTF's rules and ethics

## Contribution Process

### 1. Fork and Clone
```bash
git clone https://github.com/your-username/WTF.git
cd WTF
```

### 2. Create a Branch
```bash
git checkout -b writeup/event-name-challenge-name
```

### 3. Use the Template
Copy `WRITEUP_TEMPLATE.md` to create your writeup:
```bash
cp WRITEUP_TEMPLATE.md Category/challenge-name.md
```

### 4. Write Your Writeup
Follow the template structure and guidelines below.

### 5. Submit Pull Request
- Use descriptive commit messages
- Reference any related issues
- Provide a clear PR description

## Writeup Quality Standards

### Required Elements
- **Clear title** with challenge name
- **Category and metadata** (points, author, event)
- **Challenge description** (original text)
- **Detailed solution** with step-by-step explanation
- **Flag** (if appropriate to share)
- **Tools used** with versions when relevant

### Best Practices
- **Explain your thinking**: Don't just show commands, explain why
- **Include screenshots**: Especially for GUI-based challenges
- **Provide context**: Background information for complex topics
- **Code formatting**: Use proper syntax highlighting
- **Clean presentation**: Proper markdown formatting

### File Organization
```
Category/
├── challenge-name.md           # Main writeup
├── challenge-name/            # Supporting files (optional)
│   ├── exploit.py
│   ├── screenshots/
│   └── extracted-files/
```

## Content Guidelines

### What to Include
- ✅ Educational explanations
- ✅ Learning resources and references  
- ✅ Alternative solution approaches
- ✅ Lessons learned
- ✅ Tool usage and methodology

### What to Avoid
- ❌ Spoilers without proper warning
- ❌ Offensive or inappropriate content
- ❌ Copyrighted material without permission
- ❌ Personal information or credentials
- ❌ Malicious code or exploits for active systems

## Technical Requirements

### File Naming
- Use kebab-case: `challenge-name.md`
- Avoid spaces and special characters
- Be descriptive but concise

### Markdown Style
- Use headers appropriately (H1 for title, H2 for sections)
- Code blocks with language specification
- Proper linking syntax
- Alt text for images

### Code Standards
- Comment your code thoroughly
- Use meaningful variable names
- Include error handling where appropriate
- Test code before submitting

## Review Process

1. **Automated checks**: Basic formatting and link validation
2. **Peer review**: Community feedback on clarity and accuracy
3. **Maintainer review**: Final approval from repository maintainers

## Getting Help

- **Questions**: Open an issue with the `question` label
- **Discussion**: Use GitHub Discussions for general topics
- **Issues**: Report problems with the `bug` label

## Recognition

Contributors will be acknowledged in:
- Individual writeup bylines
- Repository contributors list
- Annual recognition (if applicable)

## Code of Conduct

- Be respectful and professional
- Provide constructive feedback
- Support learning and knowledge sharing
- Follow responsible disclosure practices

---

Thank you for helping make this repository a valuable learning resource! 🎓