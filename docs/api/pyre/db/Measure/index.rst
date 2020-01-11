:mod:`pyre.db.Measure`
======================

.. py:module:: pyre.db.Measure


Module Contents
---------------

.. py:class:: Measure

   Bases: :class:`pyre.records.measure`

   The base class for table field descriptors

   .. py:class:: measure

      The base class of the local mixins.

      Its purpose is to trap value coercion and skip it for the special values {NULL} and
      {DEFAULT} that show up as {literals} instances

      .. method:: coerce(self, value, **kwds)




   .. py:class:: bool

      Bases: :class:`pyre.db.Measure.measure`

      Mixin for booleans

      .. attribute:: decl
         :annotation: = BOOLEAN

         

      .. method:: sql(self, value)


         SQL rendering of {value}



   .. py:class:: date(default=None, **kwds)

      Bases: :class:`pyre.db.Measure.measure`

      Mixin for dates

      .. attribute:: decl
         :annotation: = DATE

         

      .. method:: sql(self, value)


         SQL rendering of {value}



   .. py:class:: decimal(precision, scale, **kwds)

      Bases: :class:`pyre.db.Measure.measure`

      Mixin for fixed point numbers

      .. method:: decl(self)
         :property:


         SQL rendering of my type name


      .. method:: sql(self, value)


         SQL rendering of {value}



   .. py:class:: float

      Bases: :class:`pyre.db.Measure.measure`

      Mixin for floating point numbers

      .. attribute:: decl
         :annotation: = DOUBLE PRECISION

         

      .. method:: sql(self, value)


         SQL rendering of my value



   .. py:class:: int

      Bases: :class:`pyre.db.Measure.measure`

      Mixin for integers

      .. attribute:: decl
         :annotation: = INTEGER

         

      .. method:: sql(self, value)


         SQL rendering of my value



   .. py:class:: str(maxlen=None, **kwds)

      Bases: :class:`pyre.db.Measure.measure`

      Mixin for strings

      .. method:: decl(self)
         :property:


         SQL rendering of my type name


      .. method:: sql(self, value)


         SQL rendering of my value



   .. py:class:: time(default=None, timezone=False, **kwds)

      Bases: :class:`pyre.db.Measure.measure`

      Mixin for timestamps

      .. method:: decl(self)
         :property:


         SQL rendering of my type name


      .. method:: sql(self, value)


         SQL rendering of {value}



   .. attribute:: _primary
      

      

   .. attribute:: _unique
      

      

   .. attribute:: _notNull
      

      

   .. attribute:: _foreign
      

      

   .. method:: setDefault(self, value)


      Set a new default value


   .. method:: primary(self)


      Mark a field as a primary key


   .. method:: unique(self)


      Mark a field as containing values that are unique across the table rows


   .. method:: notNull(self)


      Mark a field as not accepting a NULL value


   .. method:: references(self, **kwds)


      Mark a field as a foreign key


   .. method:: decldefault(self)


      Invoked by the SQL mill to create the declaration of the default value



