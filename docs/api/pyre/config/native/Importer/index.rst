:mod:`pyre.config.native.Importer`
==================================

.. py:module:: pyre.config.native.Importer


Module Contents
---------------

.. py:class:: Importer

   Bases: :class:`pyre.config.Loader.Loader`

   This component codec recognizes uris of the form

       import:package.subpackage.factory#name

   The uri is interpreted as if

       from package.subpackage import factory
       factory(name=name)

   had been issued to the interpreter. {factory} is expected to be either a component class or
   a function that returns a component class. This class is then instantiated using {name} as
   the sole argument to the constructor. If {name} is not present, the component class is
   returned.

   .. attribute:: schemes
      :annotation: = ['import']

      

   .. method:: load(cls, uri, **kwds)
      :classmethod:


      Interpret {uri} as a module to be loaded


   .. method:: locateShelves(cls, protocol, scheme, context, **kwds)
      :classmethod:


      Locate candidate shelves for the given {uri}


   .. method:: interpret(cls, request)
      :classmethod:


      Attempt to extract to extract a resolution context and a symbol from the {request}


   .. method:: assemble(cls, context)
      :classmethod:


      Assemble the sequence of directories in to a form suitable for the address part of a uri


   .. method:: prime(cls, linker)
      :classmethod:


      Build my initial set of shelves



