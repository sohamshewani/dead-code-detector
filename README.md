Dead Code Detector is a multi-component CLI utility designed to analyze Python code for dead code, store the analysis in a SQLite database, and test API performance under concurrent requests. The architecture is modular and designed for ease of maintenance and extension. Each component is well-documented and includes comprehensive tests to ensure reliability and correctness.

## Architecture Overview

### Core Module
- **AST Analysis:** Uses the `astroid` library to parse and analyze Python code for dead code.
- **Database Operations:** Utilizes `sqlite3` for storing and retrieving analyzed code.
- **Stress Testing:** Implements an asynchronous stress tester using `pytest-asyncio` to evaluate API performance under concurrent requests.

### CLI Module
- Provides a rich terminal interface using the `click` and `rich` libraries.
- Serves as the main entry point for the application, delegating tasks to the core module.

### Test Suite
- Ensures the core module functions correctly and handles various edge cases.
- Includes tests for the AST analysis, database operations, and stress testing components.

## Installation

To install the package, use pip:
```
pip install -r requirements.txt
```

## Usage

Run the application using the following command:
```
dead-code-detector [options]
```

### Options
- `--help`: Display help information.
- `--file <file_path>`: Analyze a specific Python file.
- `--directory <directory_path>`: Analyze all Python files in a directory.
- `--stress-test <url> <count>`: Perform a stress test on the specified API URL with the given number of concurrent requests.

## Contributing

Contributions are welcome! Please refer to the CONTRIBUTING.md file for guidelines on how to contribute to the project.

## License

This project is licensed under the MIT License - see the LICENSE file for details.