# Contributing to Status 246

Thank you for your interest in contributing to the Status 246 specification! This project aims to standardize HTTP status code 246 "Guardrail Check Failed" for AI and ML systems.

## Ways to Contribute

### 📝 Specification Feedback

Help us improve the core specification:
- Review the [draft specification](specification/draft.md)
- Open issues for questions, suggestions, or ambiguities
- Participate in [GitHub Discussions](https://github.com/status246/specification/discussions)
- Join our [monthly community calls](community/meetings.md)

### 💻 Reference Implementations

We need implementations across languages and frameworks to demonstrate real-world viability:

**Current Status:**
- ✅ JavaScript (Express.js) - Complete
- ✅ Python (FastAPI) - Complete  
- 🚧 Java (Spring Boot) - In Progress
- 📋 Go, Ruby, PHP, .NET - Help Wanted!

**Implementation Requirements:**
- Follow the [specification](specification/draft.md) exactly
- Include comprehensive tests covering edge cases
- Provide clear documentation and examples
- Handle both success (200) and guardrail failure (246) cases
- Include error handling for malformed responses

### 📚 Documentation

Help make Status 246 accessible to developers:
- Implementation guides for specific platforms
- Migration guides from existing error handling patterns
- Use case documentation and real-world examples
- FAQ improvements based on community questions

### 🐛 Issues and Bug Reports

Help us identify and fix problems:
- Specification ambiguities or contradictions
- Documentation gaps or errors
- Implementation bugs or inconsistencies
- Security considerations we haven't addressed

## Getting Started

### For Specification Contributors

1. **Read the current draft** - [specification/draft.md](specification/draft.md)
2. **Check existing issues** - See what's already being discussed
3. **Join discussions** - Share your perspective on open questions
4. **Propose changes** - Open issues or submit PRs with improvements

### For Implementation Contributors

1. **Choose a platform** - Pick from our [needed implementations list](#reference-implementations)
2. **Review existing implementations** - See [implementations/](implementations/) for examples
3. **Follow the template** - Each implementation should include:
   - README with setup instructions
   - Core library/middleware for Status 246 support
   - Example application demonstrating usage
   - Test suite covering specification requirements
   - Documentation for integration

### For Documentation Contributors

1. **Identify gaps** - What's confusing or missing?
2. **Check the docs folder** - See [docs/](docs/) for current documentation
3. **Write clear examples** - Real-world scenarios help developers understand
4. **Test instructions** - Make sure setup guides actually work

## Submission Process

### Pull Requests

1. **Fork the repository**
2. **Create a feature branch**
   ```bash
   git checkout -b feature/add-ruby-implementation
   ```
3. **Make your changes**
   - Follow existing code style and patterns
   - Add tests for new functionality
   - Update relevant documentation
4. **Test thoroughly**
   - Run existing test suites
   - Test your changes in isolation
   - Verify examples work as documented
5. **Submit a pull request**
   - Use clear, descriptive titles
   - Reference related issues
   - Explain the motivation and approach

### Issues

When opening an issue, please include:
- **Clear title** describing the problem or suggestion
- **Context** - What you were trying to do
- **Expected behavior** vs **actual behavior**
- **Platform/language** if relevant
- **Code samples** or links to reproduce the issue

## Code Style Guidelines

### General Principles
- **Clarity over cleverness** - Code should be easy to understand
- **Follow language conventions** - Use established patterns for each platform
- **Comprehensive documentation** - Every public function/method should be documented
- **Error handling** - Gracefully handle edge cases and malformed input

### Language-Specific Guidelines
- **JavaScript**: Follow [Airbnb Style Guide](https://github.com/airbnb/javascript)
- **Python**: Follow [PEP 8](https://pep8.org/) and use type hints
- **Java**: Follow [Google Java Style](https://google.github.io/styleguide/javaguide.html)
- **Go**: Follow [Effective Go](https://golang.org/doc/effective_go.html)

## Community Standards

### Code of Conduct

We follow the [Contributor Covenant Code of Conduct](CODE_OF_CONDUCT.md). By participating, you agree to uphold this code.

### Communication Guidelines

- **Be respectful and inclusive**
- **Focus on technical merit**
- **Provide constructive feedback**
- **Help newcomers get started**
- **Stay on topic** in discussions

### Decision Making

- **Consensus-driven** - We seek broad agreement on changes
- **Technical merit** - Decisions based on technical soundness
- **Real-world impact** - Consider how changes affect actual implementations
- **Backwards compatibility** - Avoid breaking existing implementations

## Recognition

Contributors will be:
- **Listed in specification acknowledgments**
- **Added to the project contributors page**
- **Invited to community calls and working sessions**
- **Recognized in release notes** for significant contributions

## Development Setup

### Repository Structure
```
status246-specification/
├── specification/          # Core specification documents
├── implementations/        # Reference implementations
├── examples/              # Usage examples and demos
├── docs/                  # Documentation and guides
├── tools/                 # Validation and testing tools
└── community/             # Community resources and meeting notes
```

### Testing

Each implementation should include:
- **Unit tests** for core functionality
- **Integration tests** with example applications
- **Specification compliance tests** verifying correct behavior
- **Performance benchmarks** where relevant

## Questions and Support

- **Technical questions**: [GitHub Discussions](https://github.com/status246/specification/discussions)
- **Real-time chat**: [Discord Server](#)
- **Implementation help**: Tag [@portkey-ai] in issues
- **Specification questions**: Open an issue with the `specification` label

## Roadmap and Priorities

Current priorities (help wanted!):
1. **Additional language implementations** (Go, Ruby, PHP, .NET)
2. **Real-world adoption** (get more organizations using Status 246)
3. **Tooling** (validation libraries, testing utilities)
4. **Documentation** (migration guides, best practices)
5. **Standards submission** (IETF Internet-Draft preparation)

Thank you for helping make Status 246 a reality! 🚀
