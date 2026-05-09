Run the test suite for this project.

## Environment

This project uses:
- **pyenv** for Python version management (version specified in `.python-version`)
- **venv** at `.venv/` for dependencies

The correct Python interpreter is `.venv/bin/python`.

## Running tests

Run all tests:
```
.venv/bin/python -m pytest
```

Run a specific test file:
```
.venv/bin/python -m pytest custom_components/gardena_smart_system/<test_file>.py
```

Run a specific test:
```
.venv/bin/python -m pytest custom_components/gardena_smart_system/<test_file>.py::<TestClass>::<test_method>
```

## Configuration

- pytest config is in `pytest.ini`
- Test files are in `custom_components/gardena_smart_system/test_*.py`
- Coverage is configured for `custom_components/gardena_smart_system`

## Notes

- Do NOT use the system `python` or `pytest` directly - always use `.venv/bin/python -m pytest`
- The `--disable-socket` plugin is active (network calls are blocked in tests)
- asyncio_mode is set to `auto`
