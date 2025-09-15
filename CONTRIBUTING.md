# Contributing to Spatial Dynamics

Thank you for your interest in contributing to Spatial Dynamics! We welcome contributions from the community and are excited to work with you.

## Table of Contents

- [Code of Conduct](#code-of-conduct)
- [Getting Started](#getting-started)
- [Development Setup](#development-setup)
- [Making Changes](#making-changes)
- [Testing](#testing)
- [Submitting Changes](#submitting-changes)
- [Style Guidelines](#style-guidelines)
- [Reporting Issues](#reporting-issues)
- [Feature Requests](#feature-requests)

## Code of Conduct

By participating in this project, you agree to abide by our Code of Conduct. Please be respectful, inclusive, and constructive in all interactions.

## Getting Started

1. **Fork the repository** on GitHub
2. **Clone your fork** locally:
   ```bash
   git clone https://github.com/e-esteva/spatial-dynamics.git
   cd spatial-dynamics
   ```
3. **Add the original repository** as upstream:
   ```bash
   git remote add upstream https://github.com/e-esteva/spatial-dynamics.git
   ```

## Development Setup

1. **Create a virtual environment**:
   ```bash
   python -m venv venv
   source venv/bin/activate  # On Windows: venv\Scripts\activate
   ```

2. **Install the package in development mode**:
   ```bash
   pip install -e .
   ```

3. **Install development dependencies**:
   ```bash
   pip install pytest black flake8 mypy
   ```

## Making Changes

1. **Create a new branch** for your feature or bugfix:
   ```bash
   git checkout -b feature/your-feature-name
   # or
   git checkout -b fix/issue-description
   ```

2. **Keep your branch up to date** with upstream:
   ```bash
   git fetch upstream
   git rebase upstream/main
   ```

3. **Make your changes** following the style guidelines below

4. **Write or update tests** for your changes

5. **Update documentation** if necessary

## Testing

We use pytest for testing. Please ensure all tests pass before submitting your changes.

**Run all tests**:
```bash
pytest
```

**Run tests with coverage**:
```bash
pytest --cov=spatial_dynamics
```

**Run specific test files**:
```bash
pytest tests/test_n_simplex.py
pytest tests/test_pairwise.py
```

### Writing Tests

- Write tests for all new functionality
- Ensure tests are descriptive and cover edge cases
- Place tests in the appropriate file in the `tests/` directory
- Follow the existing test patterns and naming conventions

## Submitting Changes

1. **Ensure your code passes all tests**:
   ```bash
   pytest
   ```

2. **Format your code**:
   ```bash
   black .
   flake8 .
   ```

3. **Type check your code** (if applicable):
   ```bash
   mypy spatial_dynamics/
   ```

4. **Commit your changes** with a clear, descriptive message:
   ```bash
   git add .
   git commit -m "Add feature: brief description of what you added"
   ```

5. **Push to your fork**:
   ```bash
   git push origin feature/your-feature-name
   ```

6. **Create a Pull Request** on GitHub:
   - Provide a clear title and description
   - Reference any related issues
   - Include screenshots or examples if applicable

## Style Guidelines

### Python Code Style

- Follow **PEP 8** standards
- Use **Black** for code formatting (line length: 88 characters)
- Use **type hints** where appropriate
- Write **docstrings** for all public functions, classes, and modules

### Docstring Format

Use Google-style docstrings:

```python
def example_function(param1: int, param2: str) -> bool:
    """Brief description of the function.
    
    Longer description if needed.
    
    Args:
        param1: Description of param1.
        param2: Description of param2.
    
    Returns:
        Description of return value.
    
    Raises:
        ValueError: When something goes wrong.
    """
    pass
```

### Commit Message Guidelines

- Use the present tense ("Add feature" not "Added feature")
- Use the imperative mood ("Move cursor to..." not "Moves cursor to...")
- Limit the first line to 72 characters or less
- Reference issues and pull requests liberally after the first line

Examples:
```
Add n-simplex neighborhood calculation

Fix edge case in pairwise distance computation

Update README with installation instructions

Closes #123
```

## Reporting Issues

When reporting issues, please include:

- **Clear description** of the problem
- **Steps to reproduce** the issue
- **Expected behavior** vs actual behavior
- **Environment information**:
  - Python version
  - Operating system
  - Package version
  - Relevant dependencies

Use the GitHub issue template if available.

## Feature Requests

We welcome feature requests! When submitting one, please:

- **Check existing issues** to avoid duplicates
- **Describe the feature** clearly and concisely
- **Explain the use case** and why it would be valuable
- **Consider implementation** if you have ideas

## Development Tips

- **Keep changes focused**: One feature or fix per pull request
- **Write meaningful commit messages**: Help others understand your changes
- **Test thoroughly**: Consider edge cases and different input types
- **Document your code**: Clear docstrings and comments help everyone
- **Ask questions**: Don't hesitate to open an issue for clarification

## Getting Help

- **GitHub Issues**: For bug reports and feature requests
- **GitHub Discussions**: For questions and general discussion
- **Code Review**: We'll provide feedback on pull requests

## Recognition

Contributors will be acknowledged in the project. Thank you for helping make Spatial Dynamics better!

---
