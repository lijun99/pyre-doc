:mod:`pyre.units.Dimensional`
=============================

.. py:module:: pyre.units.Dimensional


Module Contents
---------------

.. py:class:: Dimensional(value, derivation)

   This class comprises the fundamental representation of quantities with units

   .. attribute:: fundamental
      :annotation: = ['kg', 'm', 's', 'A', 'K', 'mol', 'cd']

      

   .. attribute:: zero
      

      

   .. attribute:: value
      :annotation: = 0

      

   .. attribute:: derivation
      

      

   .. method:: isCompatible(self, other)


      Predicate that checks whether {other} has the same derivation as I do


   .. method:: __add__(self, other)


      Addition


   .. method:: __sub__(self, other)


      Subtraction


   .. method:: __mul__(self, other)


      Multiplication


   .. method:: __truediv__(self, other)


      True division


   .. method:: __pow__(self, other)


      Exponentiation


   .. method:: __pos__(self)


      Unary plus


   .. method:: __neg__(self)


      Unary minus


   .. method:: __abs__(self)


      Absolute value


   .. method:: __rmul__(self, other)


      Right multiplication


   .. method:: __rtruediv__(self, other)


      Right division


   .. method:: __float__(self)


      Conversion to float


   .. method:: __lt__(self, other)


      Ordering: less than


   .. method:: __le__(self, other)


      Ordering: less than or equal to


   .. method:: __eq__(self, other)


      Ordering: equality


   .. method:: __ne__(self, other)


      Ordering: not equal to


   .. method:: __gt__(self, other)


      Ordering: greater than


   .. method:: __ge__(self, other)


      Ordering: greater than or equal to


   .. method:: __str__(self)


      Conversion to str


   .. method:: __format__(self, code)


      Formatting support

      The parameter {code} is a string of the form
          value={format_spec},base={scale},label={label}
      where
          {format_spec}: a format specification appropriate for representing floats
          {scale}: a dimensional quantity to be used as a scale for the value
          {label}: the label with units that should follow the magnitude of the quantity

      Example:
          >>> from pyre.units.SI import m,s
          >>> g = 9.81*m/s
          >>> "{accel:value=.2f,base={scale},label=g}".format(accel=100*m/s**2, scale=g)
          '10.2 g'


   .. method:: _strDerivation(self)


      Build a representation of the fundamental unit labels raised to the exponents specified
      in my derivation.

      The unit parser can parse this textual representation and convert it back into a
      dimensional quantity.



.. data:: fundamental
   

   

.. data:: zero
   

   

