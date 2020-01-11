:mod:`pyre.flow`
================

.. py:module:: pyre.flow

.. autoapi-nested-parse::

   Support for workflows



Submodules
----------
.. toctree::
   :titlesonly:
   :maxdepth: 1

   Binder/index.rst
   Factory/index.rst
   Node/index.rst
   Producer/index.rst
   Product/index.rst
   Specification/index.rst
   Status/index.rst
   Workflow/index.rst


Package Contents
----------------

.. py:class:: producer

   Bases: :class:`pyre.protocol`

   The requirements that all factories must implement

   .. method:: make(self, **kwds)


      Build all products


   .. method:: plan(self, **kwds)


      Describe what needs to get to done to make the products



.. py:class:: specification

   Bases: :class:`pyre.protocol`

   The protocol of product specifications

   Specifications are snapshots of product attributes

   .. attribute:: input
      :annotation: = False

      

   .. attribute:: output
      :annotation: = False

      

   .. method:: blueprint(cls, **kwds)
      :classmethod:


      Make an input descriptor


   .. method:: product(cls, **kwds)
      :classmethod:


      Make an output descriptor



.. py:class:: factory

   Bases: :class:`pyre.flow.Node.Node`

   The base class for creators of data products

   .. method:: make(self, context=None)


      Construct my products


   .. method:: plan(self, context=None)


      Describe what needs to get to done to make my products



.. py:class:: product

   Bases: :class:`pyre.flow.Node.Node`

   The base class for data products

   .. method:: sync(self)


      Examine my state



.. py:class:: bind(method, inputs=None, outputs=None, **kwds)

   Method decorator that constructs {operator} nodes to connect {inputs} to {outputs}

   .. attribute:: method
      

      

   .. attribute:: inputs
      

      

   .. attribute:: outputs
      

      

   .. method:: __get__(self, instance, cls)


      Access to the method



.. py:class:: workflow

   Bases: :class:`pyre.application`

   A simple application class for managing workflows

   .. attribute:: factories
      

      

   .. attribute:: doc
      :annotation: = the set of flow factories

      

   .. attribute:: products
      

      

   .. attribute:: doc
      :annotation: = the set of flow products

      


