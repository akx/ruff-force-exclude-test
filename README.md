# ruff --force-exclude bug test repo

* There are no excludes in `pyproject.toml`.
* Running `ruff .` shows the F401 error, as expected.
* Running `ruff foo/a.py` shows the F401 error, as expected.
* Running `ruff --force-exclude .` claims there are no Python files. This shouldn't happen since nothing is excluded.
* Running `ruff --force-exclude foo/a.py` claims there are no Python files. This shouldn't happen since nothing is excluded.

