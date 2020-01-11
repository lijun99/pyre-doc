:mod:`pyre.config.Loader`
=========================

.. py:module:: pyre.config.Loader


Module Contents
---------------

.. py:class:: Loader

   Base class for strategies that build component descriptors from persistent stores

   .. method:: loadShelves(cls, executive, protocol, uri, scheme, context, **kwds)
      :classmethod:


      Locate and load shelves for the given {uri}; if the {uri} is not sufficiently qualified
      to point to a unique location, use {protocol} to form plausible candidates.


   .. method:: locateShelves(cls, executive, protocol, scheme, context, symbol, cfgpath=None, **kwds)
      :classmethod:


      Locate candidate shelves for the given {uri}


   .. method:: register(cls, index)
      :classmethod:


      Register the recognized schemes with {index}


   .. method:: prime(cls, linker)
      :classmethod:


      Build my initial set of shelves



