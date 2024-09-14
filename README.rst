doccmd-pre-commit
=================

A pre-commit hook for doccmd.

Using doccmd with pre-commit
----------------------------

To run doccmd with pre-commit, add hooks like the following to your `.pre-commit-config.yaml`:

.. code-block:: yaml

   -   repo: https://github.com/adamtheturtle/doccmd-pre-commit
       rev: v2024.9.11.5
       hooks:
       -   id: doccmd
           args: ["--language", "shell", "--command", "shellcheck --shell=bash"]
           additional_dependencies: ["shellcheck-py"]
