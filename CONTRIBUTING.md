# Contributing to UK Fuel Finder Python Library

Thank you for considering contributing to this project!

## Development Setup

1. Fork the repository
2. Clone your fork:
   ```bash
   git clone https://github.com/YOUR_USERNAME/ukfuelfinder.git
   cd ukfuelfinder
   ```

3. Install development dependencies:
   ```bash
   pip install -e .[dev]
   ```

## Code Style

- Follow PEP 8 style guidelines
- Use Ruff for linting and formatting: `ruff check ukfuelfinder tests` and `ruff format ukfuelfinder tests`
- Use type hints for all functions (checked with mypy)
- Add docstrings to all public methods

## Testing

- Write tests for all new features
- Keep coverage at or above the enforced floor (currently 70%)
- Run tests before submitting PR:
  ```bash
  pytest
  ```
- Integration tests hit the real API and are skipped by default; run them with
  credentials in `.env` via `pytest -m integration -o addopts=`

## Pull Request Process

1. Create a feature branch: `git checkout -b feature/your-feature`
2. Make your changes
3. Add tests
4. Run code quality checks:
   ```bash
   ruff check ukfuelfinder tests
   ruff format --check ukfuelfinder tests
   mypy
   pytest
   ```
5. Commit with clear messages
6. Push to your fork
7. Create a Pull Request

## Reporting Issues

- Use GitHub Issues
- Include Python version, library version, and error messages
- Provide minimal reproducible example

## Code of Conduct

Be respectful and constructive in all interactions.
