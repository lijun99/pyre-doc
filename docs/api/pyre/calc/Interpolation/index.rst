:mod:`pyre.calc.Interpolation`
==============================

.. py:module:: pyre.calc.Interpolation


Module Contents
---------------

.. py:class:: Interpolation(model, expression, **kwds)

   Support for building evaluation graphs involving the values of nodes registered with a
   {SymbolTable} instance. {Interpolation} builds its value by splicing together strings.

   .. attribute:: category
      :annotation: = interpolation

      

   .. attribute:: expression
      

      

   .. attribute:: _scanner
      

      

   .. method:: interpolations(self)
      :property:


      Return a sequence over the nodes in my dependency graph that are constructed by expanding
      the values of other nodes in a macro


   .. method:: getValue(self)


      Compute and return my value


   .. method:: setValue(self, value)


      Use the new {value} as my formula


   .. method:: identify(self, authority, **kwds)


      Let {authority} know I am an interpolation


   .. method:: compile(cls, model, expression)
      :classmethod:


      Compile {expression} and build an evaluator that resolves named references to other
      nodes against {model}.


   .. method:: expand(cls, model, expression)
      :classmethod:


      Compute the value of {expression} by expanding any references to {model} nodes



