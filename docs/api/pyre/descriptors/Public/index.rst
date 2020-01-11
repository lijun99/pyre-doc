:mod:`pyre.descriptors.Public`
==============================

.. py:module:: pyre.descriptors.Public


Module Contents
---------------

.. py:class:: Public(name=None, **kwds)

   Mix-in class that endows descriptors with a name, aliases and support for simple
   documentation

   .. attribute:: name
      

      

   .. attribute:: aliases
      

      

   .. attribute:: tip
      :annotation: = 

      

   .. method:: doc(self)
      :property:


      Return my documentation string


   .. method:: bind(self, name, **kwds)


      Called by my client after all the available meta-data have been harvested



