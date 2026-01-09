# Test Case: Poetry Conflict - .python-version vs tool.poetry.dependencies

## Package Manager
Poetry

## Python Version Detection
- **Source**: .python-version (PRIORITY #1)
- **Expected Version**: 3.12.0
- **Conflict**: tool.poetry.dependencies.python says ^3.9

## Files Present
- .python-version - 3.12.0 (SHOULD WIN)
- pyproject.toml - python = "^3.9" (SHOULD BE IGNORED)
- poetry.lock

## Test Purpose
Validate .python-version beats Poetry's python dependency.
