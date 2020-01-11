:mod:`pyre.schemata.Typed`
==========================

.. py:module:: pyre.schemata.Typed


Module Contents
---------------

.. py:class:: Typed(schemata=schemata, **kwds)

   A class decorator that embeds type decorated subclasses whose names match their {typename}

   .. method:: __call__(self, client)


      Build a class record


   .. method:: build(cls, client, schemata=schemata)
      :classmethod:


      Embed within {client} subclasses of its direct ancestor that also derive from the types in
      my {schemata}


   .. method:: pedigree(cls, client, schema)
      :classmethod:


      Build the ancestry of the client



