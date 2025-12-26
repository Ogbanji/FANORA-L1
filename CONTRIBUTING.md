# Contributing to Fanora L1

Thank you for your interest in contributing to Fanora L1! This document provides guidelines for contributing to the project.

## Code of Conduct

We are committed to providing a welcoming and inclusive environment. Please be respectful and professional in all interactions.

## Getting Started

1. **Fork the repository**
2. **Clone your fork**: `git clone https://github.com/ogbanji/fanora-l1.git`
3. **Create a branch**: `git checkout -b feature/your-feature-name`
4. **Make your changes**
5. **Test thoroughly**
6. **Submit a pull request**

## Development Setup

### Prerequisites

- Rust 1.75+
- Node.js 18+
- Avalanche CLI

### Building the Project

```bash
# Build all Rust modules
cargo build --workspace

# Build CLI
cd cli
npm install
npm run build

# Run tests
cargo test --workspace
cd ../tests
npm test
```

## Contribution Guidelines

### Code Style

**Rust**:
- Follow Rust standard style (`rustfmt`)
- Run `cargo clippy` and fix all warnings
- Add documentation comments for public APIs
- Write unit tests for new functionality

**TypeScript**:
- Follow TypeScript best practices
- Use meaningful variable names
- Add JSDoc comments for functions
- Write tests for new features

### Commit Messages

Use conventional commit format:

```
type(scope): subject

body

footer
```

**Types**:
- `feat`: New feature
- `fix`: Bug fix
- `docs`: Documentation changes
- `test`: Test additions/changes
- `refactor`: Code refactoring
- `perf`: Performance improvements
- `chore`: Maintenance tasks

**Example**:
```
feat(crypto): add stealth address generation

Implement stealth address generation using Curve25519.
Includes scan and spend keypairs with view tags for
efficient payment detection.

Closes #123
```

## Pull Request Process

1. **Update documentation** for any changed functionality
2. **Add tests** for new features
3. **Ensure all tests pass**: `cargo test --workspace && npm test`
4. **Update CHANGELOG.md** with your changes
5. **Request review** from maintainers

### PR Template

```markdown
## Description
Brief description of changes

## Type of Change
- [ ] Bug fix
- [ ] New feature
- [ ] Breaking change
- [ ] Documentation update

## Testing
Describe testing performed

## Checklist
- [ ] Code follows project style
- [ ] Tests added/updated
- [ ] Documentation updated
- [ ] CHANGELOG.md updated
```

## Reporting Issues

### Bug Reports

Include:
- **Description**: Clear description of the bug
- **Steps to reproduce**: Detailed steps
- **Expected behavior**: What should happen
- **Actual behavior**: What actually happens
- **Environment**: OS, Rust version, Node version
- **Logs**: Relevant error messages

### Feature Requests

Include:
- **Use case**: Why is this needed?
- **Proposed solution**: How should it work?
- **Alternatives**: Other approaches considered
- **Additional context**: Any other relevant information

## Security

**Do not** open public issues for security vulnerabilities.

Email security@fanora-l1.io with:
- Description of the vulnerability
- Steps to reproduce
- Potential impact
- Suggested fix (if any)

## License

By contributing, you agree that your contributions will be licensed under the Apache 2.0 License.

## Questions?

- Discord: https://discord.gg/fanora-l1
- Email: dev@fanora-l1.io
