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

   :input: ``--vdwtype <str>`` (optional)
   :default: ``rahm``
   :description:
     reference atomic van der Waals radii
     rahm (DOI: 10.1002/chem.201700610)
     truhlar (DOI: 10.1021/jp8111556)

   :charge: ``--chrg <int>`` (optional)
   :default: ``0``
   :description:
     absolute charge of the molecule (integer)

   :output:
     standard output (or to file with name ``<output>``)

.. code:: bash

	> kallisto vdw --inp <str> --chrg <int> <output>

Writre out all bonds in structure
   :command: ``bonds``

   :input: ``--inp <str>`` (optional)
   :default: ``coord`` (`Turbomole`)
   :description:
     input file in `xyz` or `Turbomole` format (string)

   :input: ``--partner <int>`` (optional)
   :description:
     write out partner for atom (indexing starts with ``0`` for the first atom)

   :input: ``--constrain`` (optional)
   :default: False
   :description:
     write out ``constrain.inp`` file in ``xtb`` format. Constrains all bonds in structure.

   :output:
     standard output (or to file with name ``<output>``)

.. code:: bash

	> kallisto bonds --inp <str> --partner <str> --constrain <output>

Sort underlying structure according to a breadth first search (BFS) algorithm with respect to connectivity
   :command: ``sort``

   :input: ``--inp <str>`` (optional)
   :default: ``coord`` (`Turbomole`)
   :description:
     input file in `xyz` or `Turbomole` format (string)

   :input: ``--start <int>`` (optional)
   :default: ``0``
   :description:
     define the start of the BFS sorting.

   :output:
     standard output (or to file with name ``<output>``)

.. code:: bash

	> kallisto sort --inp <str> --start <int> <output>
