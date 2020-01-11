:mod:`pyre.calc.Expression`
===========================

.. py:module:: pyre.calc.Expression


Module Contents
---------------

.. py:class:: Expression(model, expression, program, **kwds)

   Support for building evaluation graphs involving nodes that have names registered with an
   {SymbolTable} instance

   .. attribute:: category
      :annotation: = expression

      

   .. attribute:: expression
      

      

   .. attribute:: _model
      

      

   .. attribute:: _program
      

      

   .. attribute:: _scanner
      

      

   .. method:: expressions(self)
      :property:


      Return a sequence over the nodes in my dependency graph that are constructed out of python
      expressions involving the names of other nodes


   .. method:: getValue(self)


      Compute and return my value


   .. method:: setValue(self, value)


      Use the new {value} as my formula


   .. method:: identify(self, authority, **kwds)


      Let {authority} know I am an expression


   .. method:: compile(cls, model, expression)
      :classmethod:


      Compile {expression} and build an evaluator that resolves named references to other
      nodes against {model}.


   .. method:: expand(cls, model, expression)
      :classmethod:


      Compute the value of {expression} by expanding any references to {model} nodes



