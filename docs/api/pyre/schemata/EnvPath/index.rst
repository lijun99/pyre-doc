:mod:`pyre.schemata.EnvPath`
============================

.. py:module:: pyre.schemata.EnvPath


Module Contents
---------------

.. py:class:: EnvPath(variable, pathsep=pathsep, **kwds)

   Bases: :class:`pyre.schemata.List.List`

   A list of paths whose default value is tied to the value of an environment variable

   .. attribute:: typename
      :annotation: = envpath

      

   .. attribute:: pathsep
      

      

   .. method:: _coerce(self, value, **kwds)


      Convert {value} into an iterable



