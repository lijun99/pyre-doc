:mod:`pyre.schemata.Sequence`
=============================

.. py:module:: pyre.schemata.Sequence


Module Contents
---------------

.. py:class:: Sequence

   Bases: :class:`pyre.schemata.Container.Container`

   The base class for type declarators that are sequences of other types

   .. attribute:: open
      :annotation: = [({

      

   .. attribute:: close
      :annotation: = ])}

      

   .. attribute:: delimiter
      :annotation: = ,

      

   .. attribute:: typename
      :annotation: = sequence

      

   .. attribute:: container
      

      

   .. attribute:: complaint
      :annotation: = could not coerce {0.value!r} as a sequence

      

   .. method:: str(self, value)


      Render value as a string that can be persisted for later coercion


   .. method:: json(self, value)


      Generate a JSON representation of {value}


   .. method:: _coerce(self, value, incognito=True, **kwds)


      Convert {value} into an iterable



