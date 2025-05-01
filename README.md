# copier-uv-pythonpackage

This copier template creates a new Python package project setup with [uv](https://docs.astral.sh/uv), along with extra bells and whistles.

This is a work in progress, and at this stage is probably not conducive to anyone's workflow but mine.

- pyproject.toml
  - Includes configuration for all tools that support it
    - pytest
    - coverage
    - ruff
    - pyright
    - bump-my-version
    - black
    - uv
- Justfile
- Tests
  - pytest
  - coverage
- tox (if supporting multiple versions of Python)
- bump-my-version
- GitHub support (optional)
  - Security reporting link
  - GitHub Actions (if GitHub username is supplied)
    - CI test matrix
    - Publish action (optional)
    - Taylor's Version (optional)
- Documentation using Mkdocs 
  - Mkdocs Material theme
  - Module reference documentation via mkdocs-gen-files, mkdocs-literate-nav, and mkdocstrings
  - Mike for documentation versioning

# Usage

First make sure you have [uv](https://docs.astral.sh/uv) installed on your machine, and then clone this repository.

```bash
uvx copier copy /path/to/cloned/template /target/path/for/project
```

Your project will be created and follow-up instructions will be printed to the terminal.