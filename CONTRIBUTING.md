# Contributing to Open Source Security Catalog

Thank you for your interest in contributing to the Open Source Security Catalog! This document provides guidelines for contributing tools, updating existing entries, and maintaining the quality of our catalog.

## 🤝 How to Contribute

### 1. Adding a New Tool

To add a new tool to the catalog:

1. **Fork the repository** and create a new branch
2. **Choose the appropriate category** from the predefined categories in `schema.md`
3. **Create a new YAML file** in the relevant category directory
4. **Follow the schema** defined in `schema.md`
5. **Submit a pull request** with a clear description

### 2. Updating Existing Tools

To update an existing tool:

1. **Fork the repository** and create a new branch
2. **Edit the existing YAML file** with updated information
3. **Update the `last_updated` field** to the current date
4. **Submit a pull request** explaining the changes

### 3. Improving Documentation

We welcome improvements to:
- README.md content and structure
- Schema documentation
- Contributing guidelines
- Category definitions

## 📋 Tool Inclusion Criteria

For a tool to be included in the catalog, it must meet these criteria:

### ✅ Required Criteria
- **Open Source**: Must be licensed under an OSI-approved open source license
- **Active Development**: Must have recent commits (within the last 6 months)
- **Security Focus**: Must have a primary purpose related to security
- **Documentation**: Must have basic documentation or README
- **Community**: Must have some level of community adoption or support

### ✅ Preferred Criteria
- **Production Ready**: Suitable for production environments
- **Good Documentation**: Comprehensive documentation and examples
- **Active Community**: Active issue discussions and community support
- **Integration Examples**: Clear deployment and integration examples
- **Cross-Platform**: Works across multiple environments/platforms

### ❌ Exclusion Criteria
- **Proprietary Tools**: Commercial tools with no open source components
- **Abandoned Projects**: No commits for over 1 year
- **Security Concerns**: Known security vulnerabilities without fixes
- **Poor Documentation**: No documentation or unclear purpose

## 📝 Pull Request Guidelines

### PR Title Format
```
Add [Tool Name] to [Category]
Update [Tool Name] - [Brief Description]
Fix [Issue Description]
```

### PR Description Template
```markdown
## Description
Brief description of the changes

## Tool Information
- **Name**: [Tool Name]
- **Category**: [Category]
- **License**: [License]
- **GitHub**: [URL]

## Changes Made
- [ ] Added new tool entry
- [ ] Updated existing tool information
- [ ] Fixed documentation issues
- [ ] Other: [describe]

## Verification
- [ ] Tool meets inclusion criteria
- [ ] Schema compliance verified
- [ ] URLs are valid and accessible
- [ ] Description is accurate and concise
```

## 🔍 Review Process

All contributions are reviewed by maintainers. The review process includes:

1. **Schema Compliance**: Ensures the entry follows the defined schema
2. **Content Quality**: Verifies accuracy and completeness of information
3. **Inclusion Criteria**: Confirms the tool meets our inclusion standards
4. **Community Impact**: Considers the value to the security community

### Review Timeline
- **Initial Review**: Within 3-5 business days
- **Feedback**: Maintainers will provide feedback if changes are needed
- **Approval**: Once approved, the PR will be merged

## 🛠️ Development Setup

### Local Development
1. Fork the repository
2. Clone your fork: `git clone https://github.com/yourusername/open-source-security-catalog.git`
3. Create a new branch: `git checkout -b feature/add-new-tool`
4. Make your changes
5. Test your changes locally
6. Submit a pull request

### Schema Validation
We recommend validating your YAML files against the schema. You can use online YAML validators or tools like `yamllint` for basic validation.

## 📚 Resources

### Useful Links
- [Schema Documentation](schema.md)
- [Tool Categories](README.md#-tool-categories)
- [Open Source Initiative Licenses](https://opensource.org/licenses)

### Tools for Contributors
- **YAML Validator**: [YAML Lint](https://www.yamllint.com/)
- **License Checker**: [Choose a License](https://choosealicense.com/)
- **GitHub Search**: [Advanced Search](https://github.com/search/advanced)

## 🐛 Reporting Issues

If you find issues with existing tool entries or have suggestions for improvements:

1. **Check existing issues** to avoid duplicates
2. **Create a new issue** with a clear title and description
3. **Use appropriate labels** if available
4. **Provide context** and examples where possible

## 💬 Community Guidelines

### Code of Conduct
- Be respectful and inclusive
- Focus on constructive feedback
- Help others learn and grow
- Follow the golden rule

### Communication
- Use clear, descriptive commit messages
- Provide context in pull request descriptions
- Respond to feedback promptly and professionally
- Ask questions if anything is unclear

## 🎯 Contribution Ideas

Looking for ways to contribute? Here are some ideas:

### High Priority
- Add missing tools in underrepresented categories
- Update outdated tool information
- Improve integration examples
- Add deployment guides

### Medium Priority
- Improve documentation and README
- Add tool comparison matrices
- Create category-specific guides
- Add automation scripts

### Low Priority
- Improve visual design of documentation
- Add tool screenshots or demos
- Create video tutorials
- Translate documentation

## 📞 Getting Help

If you need help or have questions:

1. **Check the documentation** first
2. **Search existing issues** for similar questions
3. **Create a new issue** with your question
4. **Tag maintainers** if urgent

## 🙏 Recognition

Contributors will be recognized in:
- Pull request acknowledgments
- Contributor list in README (for significant contributions)
- Release notes for major updates

Thank you for contributing to the Open Source Security Catalog! Your contributions help make security more accessible and transparent for everyone.
