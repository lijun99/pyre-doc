:mod:`pyre.config.pfg`
======================

.. py:module:: pyre.config.pfg

.. autoapi-nested-parse::

   This package contains the implementation of the {pfg} reader and writer



Submodules
----------
.. toctree::
   :titlesonly:
   :maxdepth: 1

   Assignment/index.rst
   Config/index.rst
   Configuration/index.rst
   Event/index.rst
   EventContainer/index.rst
   Parser/index.rst
   Scanner/index.rst
   Section/index.rst


Package Contents
----------------

.. py:class:: pfg

   Bases: :class:`pyre.config.Codec.Codec`

   This package contains the implementation of the {pfg} reader and writer

   .. attribute:: encoding
      :annotation: = pfg

      

   .. method:: decode(cls, uri, source, locator)
      :classmethod:


      Parse {source} and return the configuration events it contains



