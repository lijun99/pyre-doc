:mod:`pyre.algebraic.Literal`
=============================

.. py:module:: pyre.algebraic.Literal


Module Contents
---------------

.. py:class:: Literal(value, **kwds)

   Class that encapsulates values encountered in expressions that are not instances of members
   of the {Node} class hierarchy.

   .. attribute:: category
      :annotation: = literal

      

   .. method:: literals(self)
      :property:


      Return a sequence of the literals in my span


   .. method:: identify(self, authority, **kwds)


      Let {authority} know I am a literal



