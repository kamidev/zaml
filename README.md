# 🚀 zaml
Fast YAML 1.2 parsing library for Python 3.10.x. 🐍

## What's This?

Proof-of-concept for my PyCon DE 2022 [talk](https://2022.pycon.de/program/DFWSQR/), 
**Speeding Up Python with Zig**, not yet recommended for production use!

Library with the following objectives:
 - [x] Written in pure Zig, importing `Python.h` headers directly, no FFI, `ctypes` or `cffi`.
 - [x] Compiled using the Zig toolchain / CLI, no other tool (eg. `clang`) required.
 - [x] Tested to be compatible with mac OSX.
 - [ ] Tested to be compatible with Linux and Windows.
 - [ ] Installable via PyPI, end-user should not require Zig toolchain locally in order to use.
 - [ ] Fastest available YAML 1.2 parser for Python.

Help wanted to achieve the full objectives, PRs welcome.

### Installing Locally

Some pre-requisites (linting etc.), `pyenv` also recommended:
```bash
pre-commit install
pre-commit run --all-files
```

The simplest possible extension module is a module with one function, that takes no arguments and returns an integer. 
This repo demonstrates a pure Zig module that does exactly that:

```bash
python -m venv .venv
source .venv/bin/activate
python setup.py develop
```

### Tests

Tests that the extension can in-fact be installed and returns the expected result:

```
python test.py
```

### Benchmark


