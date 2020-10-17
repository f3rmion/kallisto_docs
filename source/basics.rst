.. _quickstart:

-------------------
 Commandline Usage
-------------------

The `kallisto` program is intended to be applied via the commandline. 
We use `click` to build `kallisto`, which enables us to define subcommands in a clear and structured way.

.. contents::

Subcommands
===========

The most basic properties in ``kallisto`` are obtained by sub-commands: coordination numbers (cns), 
electronegativity equilibration atomic partial charges (eeq), atomic static polarizabilities (alp),
and charge dependent atomic van der Waals radii (vdw).


Coordination number
   :command: ``cns``

   :input: ``--inp <str>`` (optional)
   :default: ``coord`` (`Turbomole`)
   :description:
     input file in `xyz` or `Turbomole` format (string)

   :cntype: ``--cntype {exp, cov, erf}`` (optional)
   :default: ``cov``
   :description:
     choose between different damping functions (string)

   :output:
     standard output (or to file with name ``<output>``)

.. code:: bash

	> kallisto cns --inp <str> --cntype <str> <output>

Electronegativity equilibration atomic partial charges
   :command: ``eeq``

   :input: ``--inp <str>`` (optional)
   :default: ``coord`` (`Turbomole`)
   :description:
     input file in `xyz` or `Turbomole` format (string)

   :charge: ``--chrg <int>`` (optional)
   :default: ``0``
   :description:
     absolute charge of the molecule (integer)

   :output:
     standard output (or to file with name ``<output>``)

.. code:: bash

	> kallisto eeq --inp <str> --chrg <int> <output>

Static atomic polarizabilities
   :command: ``alp``

   :input: ``--inp <str>`` (optional)
   :default: ``coord`` (`Turbomole`)
   :description:
     input file in `xyz` or `Turbomole` format (string) 

   :charge: ``--chrg <int>`` (optional)
   :default: ``0``
   :description:
     absolute charge of the molecule (integer)

   :output:
     standard output (or to file with name ``<output>``)

.. code:: bash

	> kallisto alp --inp <str> --chrg <int> <output>


Charge dependent van der Waals radii
   :command: ``vdw``

   :input: ``--inp <str>`` (optional)
   :default: ``coord`` (`Turbomole`)
   :description:
     input file in `xyz` or `Turbomole` format (string)

   :charge: ``--chrg <int>`` (optional)
   :default: ``0``
   :description:
     absolute charge of the molecule (integer)

   :output:
     standard output (or to file with name ``<output>``)

.. code:: bash

	> kallisto vdw --inp <str> --chrg <int> <output>

