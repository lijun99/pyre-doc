:mod:`pyre.schemata.Dimensional`
================================

.. py:module:: pyre.schemata.Dimensional


Module Contents
---------------

.. py:class:: Dimensional(default=units.zero, **kwds)

   Bases: :class:`pyre.schemata.Numeric.Numeric`

   A type declarator for quantities with units

   .. attribute:: typename
      :annotation: = dimensional

      

   .. attribute:: complaint
      :annotation: = could not coerce {0.value!r} into a dimensional quantity

      

   .. attribute:: parser
      

      

   .. method:: coerce(self, value, **kwds)


      Attempt to convert {value} into a dimensional


   .. method:: json(self, value)


      Generate a JSON representation of {value}



