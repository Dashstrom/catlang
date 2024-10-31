.. role:: bash(code)
  :language: bash

*******
catlang
*******

|ci-docs| |ci-lint| |ci-tests| |pypi| |versions| |discord| |license|

.. |ci-docs| image:: https://github.com/Dashstrom/catlang/actions/workflows/docs.yml/badge.svg
  :target: https://github.com/Dashstrom/catlang/actions/workflows/docs.yml
  :alt: CI : Docs

.. |ci-lint| image:: https://github.com/Dashstrom/catlang/actions/workflows/lint.yml/badge.svg
  :target: https://github.com/Dashstrom/catlang/actions/workflows/lint.yml
  :alt: CI : Lint

.. |ci-tests| image:: https://github.com/Dashstrom/catlang/actions/workflows/tests.yml/badge.svg
  :target: https://github.com/Dashstrom/catlang/actions/workflows/tests.yml
  :alt: CI : Tests

.. |pypi| image:: https://img.shields.io/pypi/v/catlang.svg
  :target: https://pypi.org/project/catlang
  :alt: PyPI : catlang

.. |versions| image:: https://img.shields.io/pypi/pyversions/catlang.svg
  :target: https://pypi.org/project/catlang
  :alt: Python : versions

.. |discord| image:: https://img.shields.io/badge/Discord-catlang-5865F2?style=flat&logo=discord&logoColor=white
  :target: n
  :alt: Discord

.. |license| image:: https://img.shields.io/badge/license-MIT-green.svg
  :target: https://github.com/Dashstrom/catlang/blob/main/LICENSE
  :alt: License : MIT

Description
###########

How to properly talk to cat with pspsps.

Documentation
#############

Documentation is available on https://dashstrom.github.io/catlang

Installation
############

You can install :bash:`catlang` using `pipx <https://pipx.pypa.io/stable/>`_
from `PyPI <https://pypi.org/project>`_

..  code-block:: bash

  pip install pipx
  pipx ensurepath
  pipx install catlang

Usage
#####

..  code-block:: bash

  catlang --version
  catlang --help

Development
###########

Contributing
************

Contributions are very welcome. Tests can be run with :bash:`poe check`, please
ensure the coverage at least stays the same before you submit a pull request.

Setup
*****

You need to install `Poetry <https://python-poetry.org/docs/#installation>`_
and `Git <https://git-scm.com/book/en/v2/Getting-Started-Installing-Git>`_
for work with this project.

..  code-block:: bash

  git clone https://github.com/Dashstrom/catlang
  cd catlang
  poetry install --all-extras
  poetry run poe setup
  poetry shell

Poe
********

Poe is available for help you to run tasks.

..  code-block:: text

  test           Run test suite.
  lint           Run linters: ruff checker and ruff formatter and mypy.        
  format         Run linters in fix mode.
  check          Run all checks: lint, test and docs.
  check-tag      Check if the current tag match the version.
  cov            Run coverage for generate report and html.
  open-cov       Open html coverage report in webbrowser.
  docs           Build documentation.
  open-docs      Open documentation in webbrowser.
  setup          Setup pre-commit.
  pre-commit     Run pre-commit.
  commit         Test, commit and push.
  clean          Clean cache files.

Skip commit verification
************************

If the linting is not successful, you can't commit.
For forcing the commit you can use the next command :

..  code-block:: bash

  git commit --no-verify -m 'MESSAGE'

Commit with commitizen
**********************

To respect commit conventions, this repository uses
`Commitizen <https://github.com/commitizen-tools/commitizen?tab=readme-ov-file>`_.

..  code-block:: bash

  cz c

How to add dependency
*********************

..  code-block:: bash

  poetry add 'PACKAGE'

Ignore illegitimate warnings
****************************

To ignore illegitimate warnings you can add :

- **# noqa: ERROR_CODE** on the same line for ruff.
- **# type: ignore[ERROR_CODE]** on the same line for mypy.
- **# pragma: no cover** on the same line to ignore line for coverage.
- **# doctest: +SKIP** on the same line for doctest.

Uninstall
#########

..  code-block:: bash

  pipx uninstall catlang

License
#######

This work is licensed under `MIT <https://github.com/Dashstrom/catlang/blob/main/LICENSE>`_.
