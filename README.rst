doccmd-pre-commit
=================

A `pre-commit`_ hook for `doccmd`_.

Using doccmd with pre-commit
----------------------------

To run `doccmd`_ with `pre-commit`_,
add hooks like the following to your ``.pre-commit-config.yaml``:

.. code-block:: yaml

   -   repo: https://github.com/adamtheturtle/doccmd-pre-commit
       rev: v2025.4.8
       hooks:
       -   id: doccmd
           args: [
                "--language",
                "shell",
                "--command",
                "shellcheck --shell=bash",
            ]
           additional_dependencies: ["shellcheck-py"]

.. _doccmd: https://doccmd.readthedocs.io
.. _pre-commit: https://pre-commit.com
