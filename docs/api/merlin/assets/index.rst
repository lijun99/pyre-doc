:mod:`merlin.assets`
====================

.. py:module:: merlin.assets


Submodules
----------
.. toctree::
   :titlesonly:
   :maxdepth: 1

   Asset/index.rst
   AssetContainer/index.rst
   PythonModule/index.rst
   PythonPackage/index.rst


Package Contents
----------------

.. py:class:: pythonmodule

   Bases: :class:`merlin.assets.Asset.Asset`

   Encapsulation of an asset that represents a python source file

   .. attribute:: category
      :annotation: = python module

      

   .. attribute:: __slots__
      :annotation: = []

      


.. py:class:: pythonpackage

   Bases: :class:`merlin.assets.AssetContainer.AssetContainer`

   Encapsulation of a python package, i.e. a folder of python modules

   .. attribute:: category
      :annotation: = python package

      

   .. attribute:: __slots__
      :annotation: = []

      


