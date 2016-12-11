MTpy: A Python toolbox for standard Magnetotelluric (MT) data processing analysis and visualization
==================================

|Build Status| |Coverage Status| |Documentation Status|

Overview
========

This repository is forked from https://github.com/geophysics/mtpy/tree/ak on 2016-11-16.

CI/CD Tests

Documentation
=============

See the `user guide <http://mtpy.readthedocs.org/en/develop/>`__ for
installation & usage API documentation.

Requirements
============

System
~~~~~~

-  Software
-  Python 2.7+ or Python 3.5+

Developer setup
===============

1. Clone:

   -  ``git clone git_url``

2. Install the native libraries 

3. Install Python dependencies:

   ``python setup.py develop``

4. Run unit tests + PyLint

   ``./check-code.sh``

   (this script approximates what is run by Travis. You can
   alternatively run ``py.test`` yourself)

5. **(or)** Run all tests, including integration tests.

``./check-code.sh integration_tests``




License
===============

MTpy is licensed under the GPL version 3

The license agreement is contained in the repository and should be kept together with the code.



Conventions
===============

1. MTpy uses E- and B-fields (although the sensors may be confusingly named as H-sensors in EDI files)
2. [E] = microvolts/meter (muV/m)
3. [B] = nanotesla (nT)
4. [Z] = [E]/[B] = km/s
5. Apparent resistivty rho = 0.2 * T * |Z|^2  (in Ohm m)
6. Angles are given in degrees (mod 360)
7. EDI files can contain data in Z- or rho/phi-form
8. EDI files contain data from one station only
9. Coordinates are handled in decimal degrees (converted when reading)
10. Time stamps refer to UTC
11. Internal coordinates: X = North, Y = East
12. Rotations are interpreted clockwise (mathematically negative)
13. 0 degrees azimuth = North





.. |Build Status| image:: https://travis-ci.org/GeoscienceAustralia/mtpy2.svg?branch=develop
   :target: https://travis-ci.org/GeoscienceAustralia/mtpy2
.. |Coverage Status| image:: https://coveralls.io/repos/GeoscienceAustralia/mtpy2/badge.svg?branch=develop&service=github
   :target: https://coveralls.io/github/GeoscienceAustralia/mtpy2?branch=develop
.. |Documentation Status| image:: https://readthedocs.org/projects/mtpy2/badge/?version=develop
   :target: http://mtpy2.readthedocs.org/en/develop/
