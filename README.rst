=========
Thermo-ML
=========

-------------------------------------------
Thermodynamics powered by Machine Learning.
-------------------------------------------

:Author: Kota Matsuo ( `Linkedin <https://www.linkedin.com/in/kotamatsuo2015/?locale=en_US/>`_ )
:Version: $Revision: 0001 $

.. contents::


What is Thermo-ML?
===================

Thermo-ML is a python library for scientists in the field of
thermodynamics, who want to tap into the power of machine learning to
make accurate predictions. (If you have heard of CALPHAD, ChemSage,
FactSage, Thermochem, this project might interest you.)

Goal of this project
====================

There are two goals to this project:

1. Aggregate all known physical & chemical data of atoms & compounds, so they are all accessible with once click.

2. Develop an AI that can make accurate predictions about unknown properties of elements or even completely unknown compounds, by learning the hidden relationships between the properties of compounds (e.g. enthalpy, entropy, heat capacity, etc) and the properties of its constituent atoms (e.g. ionization energy, atomic number, electronegativity, atomic radius, etc) of thousands of compounds.

    2.1 Empirically & accurately deduce enthalpy of formation of any compounds just from its chemical formula (Note: My Master's thesis ;))

    2.2 Empirically & accurately deduce electronegativity of transition metals (Note: Leland C. Allen mentioned that electronegativities are infrequently used among transition metal chemists because of the difficulty in accurately obtaining it, in his paper "Electronegativity Is the Average One-Electron Energy of the Valence-Shell Electrons in Ground-State Free Atoms" )

    2.3 Empirically & accurately deduce percentage ionic character of bonds (Note: Linus Pauling said in his book that "We cannot hope to formulate an expression for the partial ionic character of bonds that will be accurate")

    2.4. Hmm what else can I do...


Road map
========

* 2021.03.06 - [Done] Started the project

* 2021.03.07 - [Done] Added “parse.py” module to parse chemical formula into its constituent atoms 

* 2021.03.XX - [In progress] Add module to get properties of atoms (e.g. ionization energy, electronegativity, atomic radius, etc).

* 2021.04.XX - [JTBD] Add module to get thermodynamic properties of compounds (e.g. enthalpy, entropy, heat capacity, etc). 

   - Idea 1: Convert JANAF database to ML readable format

   - Idea 2: Convert open Thermo-Calc Database Format (TDB) to ML readable format

* 2021.05.XX - [JTBD] Add AI module that predicts enthalpy of formation of compounds just from its chemical formula, using properties of its constituent atoms.

   - Idea 1: Multilinear regression w/ constraints

   - Idea 2: Quadratic programming w/ constraints
   
   - Idea 3: Symbolic regression + genetic programming
   
   - Idea 4: Deep Learning

* 2021.06.XX - [JTBD] Add AI module that predicts electronegativity of all elements, including transition metals.

* 2021.07.XX - [JTBD] Add AI module that predicts percentage ionic character of bonds.

* 2021.08.XX - [JTBD] Add AI module that predicts entropy of formation of compounds just from its chemical formula, using properties of its constituent atoms.


Installation
============

1. Clone the repository using

``git clone https://github.com/soap-tastes-ok/thermo-ml.git``

2. Install all required dependencies using

``pip install -r /your/directory/thermo-ml/requirements.txt``

3. Append library path to system path

::

   import sys
   package = '/your/directory/thermo-ml'
   if package not in sys.path:
       sys.path.append(package)

Examples
========

1. Parsing chemical formula into atoms
--------------------------------------

To parse a chemical formula into it's constituent atoms, use the `ChemParser` module.

.. code-block:: python
    
    >>> from thermo_ml import parse
    >>> CP = parse.ChemParser()
    >>> CP.atoms("Ca2SiO3(OH)2")
    [{'Ca': 2.0, 'Si': 1.0, 'O': 5.0, 'H': 2.0}]

2. Retrieve physical & chemical properties of atoms
---------------------------------------------------

TBD

3. ...
-----

TBD


Who’s the author?
=================

I’m currently a machine learning engineer (director of AI Dev in a
startup in Tokto) who was previously doing research in computational
thermodynamics @McGill University. (`Linkedin <https://www.linkedin.com/in/kotamatsuo2015/?locale=en_US/>`_)

I will work on this during weekends, so please wait patiently. If you are
interested to follow this project, please hit the star to let me know
you are there and I’ll try to work faster ;)


Citation
========

To cite Thermo-ML in publications, please use::

    Kota Matsuo and Contributors (2021-). Thermo-ML: Thermodynamics powered with Machine learning.
    https://github.com/soap-tastes-ok/thermo-ml.git.