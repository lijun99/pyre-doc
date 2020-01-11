:mod:`pyre.config.odb.ODB`
==========================

.. py:module:: pyre.config.odb.ODB


Module Contents
---------------

.. py:class:: ODB

   Bases: :class:`pyre.config.Loader.Loader`

   This component codec recognizes uris of the form

       vfs:/path/module.py/factory#name
       file:/path/module.py/factory#name

   which is interpreted as a request to import the file {module.py} from the indicated path,
   look for the symbol {factory}, and optionally instantiate whatever component class is
   recovered using {name}

   .. attribute:: suffix
      :annotation: = .py

      

   .. attribute:: schemes
      :annotation: = ['vfs', 'file']

      

   .. method:: load(cls, executive, uri, **kwds)
      :classmethod:


      Interpret {uri} as a shelf to be loaded


   .. method:: locateShelves(cls, executive, protocol, scheme, context, **kwds)
      :classmethod:


      Locate candidate shelves from the given {uri}


   .. method:: interpret(cls, request)
      :classmethod:


      Attempt to extract a resolution context and a symbol from the {request}


   .. method:: assemble(cls, context)
      :classmethod:


      Assemble the sequence of directories in {context} to a form suitable for the address part
      of a uri



