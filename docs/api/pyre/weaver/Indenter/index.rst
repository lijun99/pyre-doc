:mod:`pyre.weaver.Indenter`
===========================

.. py:module:: pyre.weaver.Indenter


Module Contents
---------------

.. py:class:: Indenter(indenter=None, **kwds)

   A mix-in class that keeps track of the indentation level

   .. attribute:: leader
      :annotation: = 

      

   .. attribute:: INDENTER
      

      

   .. attribute:: _level
      :annotation: = 0

      

   .. attribute:: _indenter
      

      

   .. method:: indent(self, increment=1)


      Increase the indentation level by one


   .. method:: outdent(self, decrement=1)


      Decrease the indentation level by one


   .. method:: place(self, line)




