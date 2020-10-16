.. _setup:

------------------------
 Setup and Installation
------------------------

This guide deal with the general setup and local installation of the ``kallisto``
program.

.. contents::

Getting the Program
===================


`kallisto` runs on `python3`

Python development setup. Install the `pyenv` python version manager:

.. code:: bash

    > curl https://pyenv.run | bash

and add this to the `~/.bashrc` and source it:

.. code:: bash

    > export PATH="~/.pyenv/bin:$PATH"
    > eval "$(pyenv init -)"
    > eval "$(pyenv virtualenv-init -)"

Setup virtual environment
-------------------------

Install the latest python versions

.. code:: bash

    > pyenv install 3.8.2
    > pyenv install 3.7.7
    > pyenv local 3.8.2 3.7.7

You could also take `conda` to build a new virtual environment, 

.. code:: bash

    > conda create --name kallisto python=3.8

however, problems could occur while running 
the test suite due to some incompatibilities between `poetry` and `conda`, which may at the time of reading already been solved.


Install `kallisto`
------------------

Clone the repository

.. code:: bash

    > git clone git@github.com:f3rmion/kallisto.git


Install a python package manager, where we choose to go with `poetry <https://python-poetry.org/>`_

.. code:: bash

    > curl -sSL https://raw.githubusercontent.com/python-poetry/poetry/master/get-poetry.py | python
    > source ~/.poetry/env

or alternatively via `pip`

.. code:: bash

    > pip install --user poetry

Now, if you haven't already done so, change into the cloned `kallisto` directory and
download the dependencies via `poetry`:

.. code:: bash

    > cd kallisto
    > poetry install

Finally install the test automation environment `nox <https://nox.thea.codes/en/stable/>`_ via `pip``

.. code:: bash

   > pip install --user --upgrade nox

Run `nox` to test the setup (this may fail when you are using `conda`).


Getting Help from ``kallisto``
==============================

Beside this manual you can check the in-program help by

.. code:: bash

  > kallisto --help


The Verbose Mode
----------------

If you think some information is missing in your calculation you can
switch to the verbose mode by using ``--verbose`` in the command line
arguments. 
