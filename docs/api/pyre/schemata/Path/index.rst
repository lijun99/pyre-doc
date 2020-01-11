:mod:`pyre.schemata.Path`
=========================

.. py:module:: pyre.schemata.Path


Module Contents
---------------

.. py:class:: Path

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



