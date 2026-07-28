# Contributing to Sudoku Solver

First off, thank you for considering contributing to the Sudoku Solver project! It's people like you that make this tool great.

## Code of Conduct

This project and everyone participating in it is governed by our [Code of Conduct](CODE_OF_CONDUCT.md). By participating, you are expected to uphold this code.

## How Can I Contribute?

### Reporting Bugs

Before creating bug reports, please check the issue list to see if the problem has already been reported. When creating a bug report, include as many details as possible:

- **Use a clear and descriptive title**
- **Describe the exact steps to reproduce the problem**
- **Provide specific examples** (e.g., sample puzzle files)
- **Describe the behavior you observed vs what you expected**
- **Include screenshots or terminal output**
- **Include your environment details** (OS, compiler version, etc.)

### Suggesting Enhancements

Enhancement suggestions are tracked as GitHub issues. When creating an enhancement suggestion:

- **Use a clear and descriptive title**
- **Provide a step-by-step description of the suggested enhancement**
- **Provide specific examples to demonstrate the steps**
- **Describe the current behavior and the new behavior you'd like**

### Pull Requests

1. **Fork the repository** and create your branch from `main`
2. **If you've added code**, add tests if applicable
3. **Ensure the code compiles** with `g++ -std=c++17 *.cpp -o SudokuSolver`
4. **Update the README.md** if needed with details of changes
5. **Issue the pull request**

## Style Guidelines

### Git Commit Messages

- Use the present tense ("Add feature" not "Added feature")
- Use the imperative mood ("Move cursor to..." not "Moves cursor to...")
- Limit the first line to 72 characters or less
- Reference issues and pull requests liberally after the first line

### C++ Style Guide

- **Indentation**: 4 spaces (no tabs)
- **Braces**: Allman style (braces on new line)
- **Naming**:
  - Classes: PascalCase (e.g., `SudokuSolver`)
  - Functions: camelCase (e.g., `solveBoard()`)
  - Variables: camelCase (e.g., `emptyCells`)
  - Constants: UPPER_CASE (e.g., `SIZE`)
- **Comments**: Use `//` for single-line, `/** */` for documentation
- **Include Guards**: `#ifndef CLASSNAME_H`
- **No global variables** - use class members
- **Const correctness** - mark methods const where possible
- **Smart pointers** - prefer over raw pointers

### Code Quality

- **DRY** - Don't Repeat Yourself
- **SOLID** principles
- **Clean Architecture** - separation of concerns
- **Proper error handling** with exceptions
- **Memory efficient** - no leaks
- **Warning-free compilation**

## Development Setup

```bash
# Clone the repository
git clone https://github.com/yourusername/sudoku-solver.git
cd sudoku-solver

# Build
make

# Run tests
make test
```

## Testing

Before submitting a pull request:

1. **Compile without warnings**: `g++ -std=c++17 -Wall -Wextra *.cpp -o SudokuSolver`
2. **Test with sample puzzles**: Try different difficulty levels
3. **Test edge cases**: Empty board, full board, invalid puzzles
4. **Test file operations**: Load, save, validate files

## Questions?

Feel free to open an issue with your question. We'll get back to you as soon as possible.

Thank you for contributing! 🎉
