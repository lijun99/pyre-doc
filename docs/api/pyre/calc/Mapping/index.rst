:mod:`pyre.calc.Mapping`
========================

.. py:module:: pyre.calc.Mapping


Module Contents
---------------

.. py:class:: Mapping(operands, **kwds)

   Mix-in class that forms the basis of the representation of mappings

   Mappings are dictionaries with arbitrary keys whose values are nodes

   .. attribute:: category
      :annotation: = mapping

      

   .. method:: operands(self)
      :property:


      Iterate over my operands


   .. method:: mappings(self)
      :property:


      Return a sequence over mappings in my dependency graph


   .. method:: getValue(self, **kwds)


      Compute and return my value


   .. method:: setValue(self, value)


      Add the {key, node} pair in {value} to the mapping


   .. method:: __getitem__(self, key)



   .. method:: __setitem__(self, key, node)



   .. method:: _substitute(self, current, replacement)


      Adjust the operands by substituting {replacement} for {current} in the set of operands



