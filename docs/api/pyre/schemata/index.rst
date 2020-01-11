:mod:`pyre.schemata`
====================

.. py:module:: pyre.schemata


Submodules
----------
.. toctree::
   :titlesonly:
   :maxdepth: 1

   Array/index.rst
   Boolean/index.rst
   Catalog/index.rst
   Complex/index.rst
   Component/index.rst
   Container/index.rst
   Date/index.rst
   Decimal/index.rst
   Dimensional/index.rst
   EnvPath/index.rst
   EnvVar/index.rst
   Float/index.rst
   Fraction/index.rst
   INet/index.rst
   InputStream/index.rst
   Integer/index.rst
   List/index.rst
   Mapping/index.rst
   Numeric/index.rst
   OutputStream/index.rst
   Path/index.rst
   Schema/index.rst
   Sequence/index.rst
   Set/index.rst
   String/index.rst
   Time/index.rst
   Timestamp/index.rst
   Tuple/index.rst
   Typed/index.rst
   URI/index.rst
   exceptions/index.rst


Package Contents
----------------

.. py:class:: identity(default=None, **kwds)

   The base class for type declarators

   .. attribute:: typename
      :annotation: = identity

      

   .. method:: default(self)
      :property:


      Grant access to my default value


   .. method:: coerce(self, value, **kwds)


      Convert the given value into a python native object


   .. method:: string(self, value)


      Render value as a string that can be persisted for later coercion


   .. method:: json(self, value)


      Generate a JSON representation of {value}



.. py:class:: bool(default=True, **kwds)

   Bases: :class:`pyre.schemata.Numeric.Numeric`

   A type declarator for booleans

   .. attribute:: typename
      :annotation: = bool

      

   .. attribute:: complaint
      :annotation: = could not coerce {0.value!r} to bool

      

   .. attribute:: xlat
      

      

   .. method:: coerce(self, value, **kwds)


      Convert {value} into a boolean



.. py:class:: complex(default=complex(), **kwds)

   Bases: :class:`pyre.schemata.Numeric.Numeric`

   A type declarator for complex numbers

   .. attribute:: typename
      :annotation: = complex

      

   .. attribute:: complaint
      :annotation: = could not coerce {0.value!r} into a complex number

      

   .. method:: coerce(self, value, **kwds)


      Attempt to convert {value} into a complex number



.. py:class:: decimal(default=decimal.Decimal(), **kwds)

   Bases: :class:`pyre.schemata.Numeric.Numeric`

   A type declarator for fixed point numbers

   .. attribute:: typename
      :annotation: = decimal

      

   .. method:: coerce(self, value, **kwds)


      Attempt to convert {value} into a decimal


   .. method:: json(self, value)


      Generate a JSON representation of {value}



.. py:class:: float(default=float(), **kwds)

   Bases: :class:`pyre.schemata.Numeric.Numeric`

   A type declarator for floats

   .. attribute:: typename
      :annotation: = float

      

   .. attribute:: complaint
      :annotation: = could not coerce {0.value!r} into a float

      

   .. method:: coerce(self, value, **kwds)


      Attempt to convert {value} into a float



.. py:class:: fraction(default=fractions.Fraction(), **kwds)

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



.. py:class:: inet(default=any, **kwds)

   Bases: :class:`pyre.schemata.Schema.Schema`

   A type declarator for internet addresses

   .. attribute:: address
      

      

   .. attribute:: any
      

      

   .. attribute:: typename
      :annotation: = inet

      

   .. attribute:: complaint
      :annotation: = could not coerce {0.value!r} into an internet address

      

   .. attribute:: regex
      

      

   .. method:: coerce(self, value, **kwds)


      Attempt to convert {value} into a internet address


   .. method:: recognize(self, family, address)


      Return an appropriate address type based on the socket family


   .. method:: parse(self, value)


      Convert {value}, expected to be a string, into an inet address


   .. method:: json(self, value)


      Generate a JSON representation of {value}



.. py:class:: int(default=int(), **kwds)

   Bases: :class:`pyre.schemata.Numeric.Numeric`

   A type declarator for integers

   .. attribute:: typename
      :annotation: = int

      

   .. attribute:: complaint
      :annotation: = could not coerce {0.value!r} into an integer

      

   .. method:: coerce(self, value, **kwds)


      Attempt to convert {value} into an integer



.. py:class:: str(default=str(), **kwds)

   Bases: :class:`pyre.schemata.Schema.Schema`

   A type declarator for strings

   .. attribute:: typename
      :annotation: = str

      

   .. attribute:: complaint
      :annotation: = could not coerce {0.value!r} into a string

      

   .. method:: coerce(self, value, **kwds)


      Attempt to convert {value} into a string



.. py:class:: date(default=datetime.date.today(), format=format, **kwds)

   Bases: :class:`pyre.schemata.Schema.Schema`

   A type declarator for dates

   .. attribute:: format
      :annotation: = %Y-%m-%d

      

   .. attribute:: typename
      :annotation: = date

      

   .. method:: coerce(self, value, **kwds)


      Attempt to convert {value} into a date


   .. method:: string(self, value)


      Render value as a string that can be persisted for later coercion


   .. method:: json(self, value)


      Generate a JSON representation of {value}



.. py:class:: dimensional(default=units.zero, **kwds)

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



.. py:class:: path

   Bases: :class:`pyre.schemata.Schema.Schema`

   A type declarator for paths

   .. attribute:: typename
      :annotation: = path

      

   .. attribute:: complaint
      :annotation: = cannot cast {0.value!r} into a path

      

   .. attribute:: cwd
      

      

   .. attribute:: root
      

      

   .. attribute:: home
      

      

   .. method:: coerce(self, value, **kwds)


      Attempt to convert {value} into a path


   .. method:: json(self, value)


      Generate a JSON representation of {value}



.. py:class:: time(default=datetime.datetime.today(), format=format, **kwds)

   Bases: :class:`pyre.schemata.Schema.Schema`

   A type declarator for timestamps

   .. attribute:: format
      :annotation: = %H:%M:%S

      

   .. attribute:: typename
      :annotation: = time

      

   .. attribute:: complaint
      :annotation: = could not coerce {0.value!r} into a time

      

   .. method:: coerce(self, value, **kwds)


      Attempt to convert {value} into a timestamp


   .. method:: string(self, value)


      Render value as a string that can be persisted for later coercion


   .. method:: json(self, value)


      Generate a JSON representation of {value}



.. py:class:: timestamp(default=datetime.datetime.today(), format=format, **kwds)

   Bases: :class:`pyre.schemata.Schema.Schema`

   A type declarator for timestamps

   .. attribute:: format
      :annotation: = %Y-%m-%d %H:%M:%S

      

   .. attribute:: typename
      :annotation: = timestamp

      

   .. attribute:: complaint
      :annotation: = could not coerce {0.value!r} into a time

      

   .. method:: coerce(self, value, **kwds)


      Attempt to convert {value} into a timestamp


   .. method:: string(self, value)


      Render value as a string that can be persisted for later coercion


   .. method:: json(self, value)


      Generate a JSON representation of {value}



.. py:class:: uri(default=locator(), scheme=None, authority=None, address=None, **kwds)

   Bases: :class:`pyre.schemata.Schema.Schema`

   Parser for resource identifiers

   .. attribute:: typename
      :annotation: = uri

      

   .. attribute:: complaint
      :annotation: = could not coerce {0.value!r} into a URI

      

   .. method:: coerce(self, value, **kwds)


      Attempt to convert {value} into a resource locator


   .. method:: json(self, value)


      Generate a JSON representation of {value}



.. py:class:: sequence

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



.. py:class:: array(default=(), **kwds)

   Bases: :class:`pyre.schemata.Schema.Schema`

   The array type declarator

   .. attribute:: typename
      :annotation: = array

      

   .. attribute:: complaint
      :annotation: = could not coerce {0.value!r} to an array

      

   .. method:: coerce(self, value, **kwds)


      Convert {value} into a tuple



.. py:class:: list

   Bases: :class:`pyre.schemata.Sequence.Sequence`

   The list type declarator

   .. attribute:: typename
      :annotation: = list

      

   .. attribute:: container
      

      


.. py:class:: set

   Bases: :class:`pyre.schemata.Sequence.Sequence`

   The set type declarator

   .. attribute:: typename
      :annotation: = set

      

   .. attribute:: container
      

      

   .. method:: json(self, value)


      Generate a JSON representation of {value}



.. py:class:: tuple

   Bases: :class:`pyre.schemata.Sequence.Sequence`

   The tuple type declarator

   .. attribute:: typename
      :annotation: = tuple

      

   .. attribute:: container
      

      


.. py:class:: mapping

   Bases: :class:`pyre.schemata.Container.Container`

   The base class for type declarators that map strings to other types

   .. attribute:: typename
      :annotation: = mapping

      

   .. attribute:: container
      

      

   .. attribute:: complaint
      :annotation: = could not coerce {0.value!r} to a mapping

      

   .. method:: _coerce(self, value, **kwds)


      Convert {value} into a container



.. py:class:: catalog

   Bases: :class:`pyre.schemata.Mapping.Mapping`

   The catalog type declarator

   .. attribute:: typename
      :annotation: = catalog

      


.. py:class:: component(protocol, default=default, **kwds)

   Bases: :class:`pyre.schemata.Schema.Schema`

   A type declarator for components

   .. attribute:: default
      

      

   .. attribute:: complaint
      :annotation: = could not coerce {0.value!r} into a component

      

   .. attribute:: protocol
      

      

   .. method:: typename(self)
      :property:


      Identify my schema through my protocol


   .. method:: coerce(self, value, **kwds)


      Attempt to convert {value} into a component class compatible with my protocol


   .. method:: string(self, value)


      Render value as a string that can be persisted for later coercion


   .. method:: json(self, value)


      Generate a JSON representation of {value}



.. py:class:: istream(default='stdin', mode=mode, **kwds)

   Bases: :class:`pyre.schemata.Schema.Schema`, :class:`pyre.framework.Dashboard.Dashboard`

   A representation of input streams

   .. attribute:: mode
      :annotation: = r

      

   .. attribute:: typename
      :annotation: = istream

      

   .. method:: coerce(self, value, **kwds)


      Attempt to convert {value} into an open input stream


   .. method:: string(self, value)


      Render value as a string that can be persisted for later coercion


   .. method:: json(self, value)


      Generate a JSON representation of {value}



.. py:class:: ostream(default='stdout', mode=mode, **kwds)

   Bases: :class:`pyre.schemata.Schema.Schema`, :class:`pyre.framework.Dashboard.Dashboard`

   A representation of input streams

   .. attribute:: mode
      :annotation: = w

      

   .. attribute:: typename
      :annotation: = ostream

      

   .. method:: coerce(self, value, **kwds)


      Attempt to convert {value} into an open input stream


   .. method:: string(self, value)


      Render value as a string that can be persisted for later coercion


   .. method:: json(self, value)


      Generate a JSON representation of {value}



.. py:class:: envvar(variable, **kwds)

   Bases: :class:`pyre.schemata.String.String`

   A type declarator for strings whose default values are associated with an environment variable

   .. attribute:: typename
      :annotation: = envvar

      


.. py:class:: envpath(variable, pathsep=pathsep, **kwds)

   Bases: :class:`pyre.schemata.List.List`

   A list of paths whose default value is tied to the value of an environment variable

   .. attribute:: typename
      :annotation: = envpath

      

   .. attribute:: pathsep
      

      

   .. method:: _coerce(self, value, **kwds)


      Convert {value} into an iterable



.. data:: basic
   

   

.. data:: composite
   

   

.. data:: containers
   

   

.. data:: meta
   

   

.. data:: schemata
   

   

.. data:: sequences
   

   

.. data:: mappings
   

   

.. data:: numeric
   

   

.. py:class:: typed(schemata=schemata, **kwds)

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



