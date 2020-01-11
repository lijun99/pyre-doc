:mod:`pyre.schemata.Fraction`
=============================

.. py:module:: pyre.schemata.Fraction


Module Contents
---------------

.. py:class:: Fraction(default=fractions.Fraction(), **kwds)

   Bases: :class:`pyre.schemata.Numeric.Numeric`

   A type declarator for fixed point numbers

   .. attribute:: typename
      :annotation: = fraction

      

   .. attribute:: ncomplaint
      :annotation: = could not coerce {0.value!r) into a fraction

      

   .. method:: coerce(self, value, **kwds)


      Attempt to convert {value} into a fraction


   .. method:: json(self, value)


      Generate a JSON representation of {value}



