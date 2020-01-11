:mod:`pyre.framework`
=====================

.. py:module:: pyre.framework

.. autoapi-nested-parse::

   This package provides access to the top level framework manager

   The implementation is split into two classes: {Executive} and {Pyre}. The former is a base
   class that defines the responsibilities of the executive; the latter the actual instance that
   manages the lifetimes of the team of managers necessary to implement all framework
   services. All this just in case you want to take ownership of how the framework services are
   deployed by creating your own executive instance and registering it in the {pyre} namespace.



Submodules
----------
.. toctree::
   :titlesonly:
   :maxdepth: 1

   Dashboard/index.rst
   Environ/index.rst
   Executive/index.rst
   FileServer/index.rst
   Linker/index.rst
   NameServer/index.rst
   Package/index.rst
   Priority/index.rst
   Pyre/index.rst
   Schema/index.rst
   Slot/index.rst
   SlotInfo/index.rst
   exceptions/index.rst


Package Contents
----------------

.. function:: executive(**kwds)

   Factory for the framework executive.

   The pyre executive builds and maintains the top-level objects that manage the various
   framework services


.. data:: _verbose
   :annotation: = False

   

.. data:: _metaclass_Slot
   

   

.. function:: debug()

   Support for debugging the framework


