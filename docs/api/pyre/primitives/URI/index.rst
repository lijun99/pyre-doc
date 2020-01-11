:mod:`pyre.primitives.URI`
==========================

.. py:module:: pyre.primitives.URI


Module Contents
---------------

.. py:class:: URI(scheme=None, authority=None, address=None, query=None, fragment=None)

   .. attribute:: _regex
      

      

   .. attribute:: __slots__
      :annotation: = ['scheme', 'authority', 'address', 'query', 'fragment']

      

   .. method:: uri(self)
      :property:


      Assemble a string from my parts


   .. method:: parse(cls, value, scheme=None, authority=None, address=None)
      :classmethod:


      Convert {value} into a {uri}


   .. method:: clone(self, scheme=None, authority=None, address=None, query=None, fragment=None)


      Make a copy of me with the indicated replacements


   .. method:: __add__(self, other)


      Enable concatenations

      N.B.: this is not {join}; it just takes my string representation, adds {other} to the
      end, and attempts to parse the result as a {uri}


   .. method:: __str__(self)




