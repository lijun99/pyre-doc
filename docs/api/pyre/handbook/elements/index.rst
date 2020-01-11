:mod:`pyre.handbook.elements`
=============================

.. py:module:: pyre.handbook.elements


Submodules
----------
.. toctree::
   :titlesonly:
   :maxdepth: 1

   Element/index.rst
   PeriodicTable/index.rst
   elements/index.rst


Package Contents
----------------

.. py:class:: Element(number, symbol, name, weight, **kwds)

   .. method:: __str__(self)


      Generate a string representation, mostly for debugging purposes



.. py:class:: PeriodicTable(**kwds)

   An encapsulation of the periodic table of elements

   .. method:: name(self, name)


      Retrieve the element with the given {name}


   .. method:: symbol(self, symbol)


      Retrieve the element with the given {symbol}


   .. method:: atomicNumber(self, z)


      Retrieve the element with the given atomic number



.. data:: periodicTable
   

   

