# copier-uv-pythonpackage

This copier template creates a new Python package project setup with [uv](https://docs.astral.sh/uv), along with extra bells and whistles.

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
Answer the prompts and your project will be generated, a git repo will be initialized, and your project
will be bootstrapped with all dependencies installed.

To complete your setup on Github: 
- Make sure to [enable security reporting](https://docs.github.com/en/code-security/security-advisories/working-with-repository-security-advisories/configuring-private-vulnerability-reporting-for-a-repository)
- If using the publish action, add a repository secret of PYPI_TOKEN with your **project scoped** access token from PyPI. 
- If using coveralls, make sure to enable the repository in your coveralls account.

!!! warning
    
    **NEVER** use a global access token in your release workflow.

