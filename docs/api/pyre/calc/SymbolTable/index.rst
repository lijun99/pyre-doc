:mod:`pyre.calc.SymbolTable`
============================

.. py:module:: pyre.calc.SymbolTable


Module Contents
---------------

.. py:class:: SymbolTable(**kwds)

   Storage and naming services for algebraic nodes

   .. attribute:: _nodes
      

      

   .. method:: keys(self)
      :property:


      Build an iterator over my registered keys


   .. method:: nodes(self)
      :property:


      Build an iterator over my registered nodes


   .. method:: expression(self, value, **kwds)


      Build an expression node


   .. method:: interpolation(self, value, **kwds)


      Build an interpolation node


   .. method:: sequence(self, nodes, **kwds)


      Build a sequence node


   .. method:: mapping(self, nodes, **kwds)


      Build a mapping node


   .. method:: variable(self, **kwds)


      Build a variable


   .. method:: literal(self, **kwds)


      Build a literal node


   .. method:: get(self, name, default=None)


      Attempt to resolve {name} and return its value; if {name} is not in the symbol table,
      bind it to {default} and return this new value


   .. method:: insert(self, name, node)


      Insert {node} in the symbol table under {name}. If there is an existing node, adjust the
      evaluation graph by replacing the existing node with the new one everywhere


   .. method:: retrieve(self, name)


      Retrieve the node registered under {name}. If no such node exists, an error marker will
      be built, stored in the symbol table under {name}, and returned.


   .. method:: __contains__(self, name)


      Check whether {name} is present in the symbol table


   .. method:: __iter__(self)


      Go through my keys


   .. method:: __getitem__(self, name)


      Look up the node registered under {name} and return its value


   .. method:: __setitem__(self, name, value)


      Add or update the named node with the given {value}



