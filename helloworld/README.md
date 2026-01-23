# helloworld (CLI)

This directory contains the package entry point for the `helloworld_in_python` command.

## Run (installed)

From the repository root:

```bash
pip install .
helloworld_in_python
```

## `--version`

```bash
helloworld_in_python --version
```

This prints `helloworld <version>`. The version comes from `helloworld/VERSION.txt` and is exposed at runtime as `helloworld.__version__`.

## Run (without installing)

From the repository root:

```bash
python helloworld.py
python helloworld.py --version
```

## Packaging notes

- Console script entry point is defined in `pyproject.toml` under `[project.scripts]`:
  - `helloworld_in_python = "helloworld.main:main"`
- Package version is single-sourced from `helloworld/VERSION.txt` (also used by `setup.py`).
