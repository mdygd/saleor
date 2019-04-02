Working with Python Code
========================

Managing Dependencies
---------------------

To guarantee repeatable installations, all project dependencies are managed using `Poetry <https://poetry.eustace.io/docs/>`_.
Project's direct dependencies are listed in ``pyproject.toml`` and running :code:`poetry lock` would generate ``poetry.lock`` that has all versions pinned.

For users who are not using Poetry, ``requirements.txt`` and ``requirements_dev.txt`` are also provided. They should be updated by :code:`poetry export --dev -f requirements.txt; mv requirements.txt requirements_dev.txt` and :code:`poetry export -f requirements.txt`, if any dependencies are added/updated. Additionally `--without-hashes` can be provided if hashes are not needed in requirement files.

We recommend you use this workflow and keep ``pyproject.toml`` as well as ``poetry.lock`` under version control to make sure all computers and environments run exactly the same code.
