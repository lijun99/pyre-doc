:mod:`pyre.calc.Datum`
======================

.. py:module:: pyre.calc.Datum


Module Contents
---------------

.. py:class:: Datum

   Bases: :class:`pyre.algebraic.AbstractNode.AbstractNode`

   The base class for nodes that have values

   .. attribute:: mapping
      

      

   .. attribute:: sequence
      

      

   .. attribute:: expression
      

      

   .. attribute:: interpolation
      

      

   .. attribute:: reference
      

      

   .. attribute:: unresolved
      

      

   .. method:: value(self)
      :property:


      Get my value


   .. method:: expressions(self)
      :property:


      Return a sequence over the nodes in my dependency graph that are constructed out of python
      expressions involving the names of other nodes


   .. method:: interpolations(self)
      :property:


      Return a sequence over the nodes in my dependency graph that are constructed by expanding
      the values of other nodes in a macro


   .. method:: mappings(self)
      :property:


      Return a sequence over the nodes in my dependency graph that are mappings


   .. method:: references(self)
      :property:


      Return a sequence over the nodes in my dependency graph that are references to other nodes


   .. method:: sequences(self)
      :property:


      Return a sequence over the nodes in my dependency graph that are sequences


   .. method:: unresolveds(self)
      :property:


      Return a sequence over the nodes in my dependency graph that represent requests for model
      names that don't exist


   .. method:: ref(self, **kwds)


      Build and return a reference to me



