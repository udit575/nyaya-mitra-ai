# Contributing to NyayaMitra

Thank you for your interest in contributing to NyayaMitra! We welcome contributions from the community to help make legal assistance more accessible.

## 🤝 How to Contribute

### Reporting Bugs

If you find a bug, please create an issue with:
- Clear description of the problem
- Steps to reproduce
- Expected vs actual behavior
- Screenshots (if applicable)
- Environment details (OS, Python version, etc.)

### Suggesting Features

We welcome feature suggestions! Please create an issue with:
- Clear description of the feature
- Use case and benefits
- Potential implementation approach

### Code Contributions

1. **Fork the Repository**
   ```bash
   git clone https://github.com/yourusername/nyayamitra.git
   cd nyayamitra
   ```

2. **Create a Branch**
   ```bash
   git checkout -b feature/your-feature-name
   ```

3. **Make Your Changes**
   - Follow the coding standards below
   - Write clear commit messages
   - Add tests for new features
   - Update documentation

4. **Test Your Changes**
   ```bash
   # Backend tests
   cd backend
   pytest
   
   # Frontend tests
   cd frontend
   npm test
   ```

5. **Commit Your Changes**
   ```bash
   git add .
   git commit -m "Add: Brief description of your changes"
   ```

6. **Push to Your Fork**
   ```bash
   git push origin feature/your-feature-name
   ```

7. **Create a Pull Request**
   - Go to the original repository
   - Click "New Pull Request"
   - Select your branch
   - Provide a clear description of changes

## 📝 Coding Standards

### Python (Backend)

- Follow PEP 8 style guide
- Use type hints
- Write docstrings for functions and classes
- Keep functions small and focused
- Use meaningful variable names

```python
def analyze_legal_document(document: str, case_type: str) -> dict:
    """
    Analyze a legal document and extract key information.
    
    Args:
        document: The document text to analyze
        case_type: Type of legal case
        
    Returns:
        Dictionary containing analysis results
    """
    # Implementation
    pass
```

### JavaScript (Frontend)

- Use ES6+ syntax
- Follow Airbnb style guide
- Use functional components with hooks
- Write clear component names
- Add PropTypes or TypeScript types

```javascript
const ChatMessage = ({ message, isUser }) => {
  return (
    <div className={isUser ? 'user-message' : 'ai-message'}>
      {message}
    </div>
  );
};
```

### Commit Messages

Use clear, descriptive commit messages:

- `Add: New feature or functionality`
- `Fix: Bug fix`
- `Update: Changes to existing feature`
- `Refactor: Code restructuring`
- `Docs: Documentation changes`
- `Test: Adding or updating tests`

Example:
```
Add: Amazon Translate integration for Hindi support

- Integrated Amazon Translate API
- Added language detection
- Updated UI with language selector
```

## 🧪 Testing Guidelines

- Write unit tests for new functions
- Ensure all tests pass before submitting PR
- Aim for >80% code coverage
- Test edge cases and error handling

## 📚 Documentation

- Update README.md if adding new features
- Add docstrings to new functions
- Update API documentation
- Include code comments for complex logic

## 🔒 Security

- Never commit API keys or credentials
- Use environment variables for sensitive data
- Report security vulnerabilities privately
- Follow AWS security best practices

## 🌟 Code Review Process

1. Maintainers will review your PR
2. Address any requested changes
3. Once approved, your PR will be merged
4. Your contribution will be acknowledged

## 💡 Areas for Contribution

We especially welcome contributions in:

- **Legal Knowledge Base**: Adding more legal documents and case laws
- **Language Support**: Adding support for regional Indian languages
- **UI/UX**: Improving user interface and experience
- **Testing**: Writing more comprehensive tests
- **Documentation**: Improving docs and tutorials
- **Performance**: Optimizing response times
- **Accessibility**: Making the app more accessible

## 📋 Pull Request Checklist

Before submitting, ensure:

- [ ] Code follows project style guidelines
- [ ] All tests pass
- [ ] New tests added for new features
- [ ] Documentation updated
- [ ] No sensitive data in commits
- [ ] Branch is up to date with main
- [ ] Clear PR description provided

## 🤔 Questions?

If you have questions:
- Check existing issues and discussions
- Create a new issue with the "question" label
- Reach out to maintainers

## 📜 Code of Conduct

- Be respectful and inclusive
- Welcome newcomers
- Focus on constructive feedback
- Respect different viewpoints
- Maintain professional communication

## 🎉 Recognition

Contributors will be:
- Listed in README.md
- Acknowledged in release notes
- Invited to join the core team (for significant contributions)

Thank you for helping make legal assistance accessible to everyone! 🙏

---

**Happy Contributing!** 🚀
