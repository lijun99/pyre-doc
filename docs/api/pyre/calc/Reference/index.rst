:mod:`pyre.calc.Reference`
==========================

.. py:module:: pyre.calc.Reference


Module Contents
---------------

.. py:class:: Reference

   A node that refers to another node

   .. attribute:: category
      :annotation: = reference

      

   .. method:: references(self)
      :property:


      Return a sequence over the nodes in my dependency graph that are references to other nodes


   .. method:: getValue(self)


      Compute and return my value


   .. method:: setValue(self, value)


      Set the value of the node i refer to


   .. method:: identify(self, authority, **kwds)


      Let {authority} know I am a reference



