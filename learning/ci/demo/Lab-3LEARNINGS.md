## Lab 3: Write Tests

### What I Learned
- Python's built-in `unittest` framework tests program behavior.
- Assertions check whether actual results match expected results.
- Tests can detect incorrect behavior even when Python code is syntactically valid.
- `subprocess.run` allows tests to execute a command-line program and check its exit code.
- Temporary directories allow CLI tests to create temporary files safely.
- An empty inventory is considered valid in this implementation.
- Duplicate server names are rejected.

### Testing Commands
- `python -m unittest discover -s . -p 'test_*.py' -v`
- `python -m ruff check .`
- `python -m ruff format --check .`

### Key Takeaway
Automated tests verify correct behavior for valid and invalid inputs and help prevent regressions when code changes.