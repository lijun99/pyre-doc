:mod:`pyre.config.cfg`
======================

.. py:module:: pyre.config.cfg

.. autoapi-nested-parse::

   This package contains the implementation of the {cfg} reader and writer



Submodules
----------
.. toctree::
   :titlesonly:
   :maxdepth: 1

   Config/index.rst
   Parser/index.rst
   Scanner/index.rst
   exceptions/index.rst


Package Contents
----------------

.. py:class:: cfg

   Bases: :class:`pyre.config.Codec.Codec`

   This package contains the implementation of the {cfg} reader and writer

   .. attribute:: encoding
      :annotation: = cfg

      

   .. method:: decode(cls, uri, source, locator)
      :classmethod:


      Parse {source} and return the configuration events it contains



