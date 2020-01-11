:mod:`pyre.framework.Linker`
============================

.. py:module:: pyre.framework.Linker


Module Contents
---------------

.. py:class:: Linker(executive, **kwds)

   Class responsible for accessing components from a variety of persistent stores

   .. attribute:: codecs
      

      

   .. attribute:: shelves
      

      

   .. method:: loadShelf(self, uri, **kwds)


      Load the shelf specified by {uri}


   .. method:: resolve(self, executive, uri, protocol, **kwds)


      Attempt to locate the component class specified by {uri}


   .. method:: indexDefaultCodecs(self)


      Initialize my codec index



