.. _quickstart:

-------------------
 Commandline Usage
-------------------

The `kallisto` program is intended to be applied via the commandline. 
We use `click` to build `kallisto`, which enables us to define subcommands in a clear and structured way.

.. contents::

Subcommands
===========

The most basic properties in ``kallisto`` are obtained by sub-commands: coordination number (cns), 
electronegativity equilibration atomic partial chare (eeq), atomic static polarizabilities (alp),
and charge dependent atomic van der Waals radii (vdw).


Coordination number
   :command: ``cns``
   :input: ``--inp <str>``
   :description:
     input file in `xyz` or `Turbomole` format (string)
   :cntype: ``--cntype {exp, cov, erf}``
   :description:
     choose between different damping functions (string)

Basic application

.. code:: bash

	> kallisto cns --inp <str> [--cntype "erf","cov","exp" {erf}] <output>

Electronegativity equilibration atomic partial charges
   :command: ``eeq``
   :input: ``--inp <str>``
   :description:
     input file in `xyz` or `Turbomole` format (string)
   :charge: ``--chrg <int>``
   :description:
     absolute charge of the molecule (integer)

Basic application

.. code:: bash

	> kallisto eeq --inp <str> [--chrg <int> {0}] <output>

Static atomic polarizabilities
   :command: ``alp``
   :input: ``--inp <str>``
   :description:
     input file in `xyz` or `Turbomole` format (string) 
   :charge: ``--chrg <int>``
   :description:
     absolute charge of the molecule (integer)

Basic application

.. code:: bash

	> kallisto alp --inp <str> [--chrg <int> {0}] <output>


Charge dependent van der Waals radii
   :command: ``vdw``
   :input: ``--inp <str>``
   :description:
     input file in `xyz` or `Turbomole` format (string)
   :charge: ``--chrg <int>``
   :description:
     absolute charge of the molecule (integer)

Basic application

.. code:: bash

	> kallisto vdw --inp <str> [--chrg <int> {0}] <output>

