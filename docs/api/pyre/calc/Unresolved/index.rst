:mod:`pyre.calc.Unresolved`
===========================

.. py:module:: pyre.calc.Unresolved


Module Contents
---------------

.. py:class:: Unresolved(request, **kwds)

   A node that raises {UnresolvedNodeError} when its value is read

   .. attribute:: category
      :annotation: = unresolved

      

   .. attribute:: request
      

      

   .. method:: unresolveds(self)
      :property:


      Return a sequence over the unresolved nodes in my dependency graph


   .. method:: getValue(self)


      Compute my value


   .. method:: identify(self, authority, **kwds)


      Let {authority} know I am an unresolved node


   .. method:: __str__(self)



   .. method:: dump(self, name, indent)




