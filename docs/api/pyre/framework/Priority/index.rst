:mod:`pyre.framework.Priority`
==============================

.. py:module:: pyre.framework.Priority


Module Contents
---------------

.. py:class:: Priority

   An intelligent enum of configuration priorities

   Each source of configuration information is assigned to a category, and each category has a
   priority. The priority is used to decide whether a the value of a trait should be modified
   based on information from the source at hand: higher priority settings override lower ones.

   Within a category, each configuration setting is assigned a rank, based on the order it was
   encountered. This kind of logic, for example, assures that command line arguments that
   appear later in the command line override earlier ones

   This class provides a resting place for the priority categories, and a total ordering so
   comparisons can be made

   .. attribute:: category
      

      

   .. attribute:: uninitialized
      

      

   .. attribute:: defaults
      

      

   .. attribute:: boot
      

      

   .. attribute:: package
      

      

   .. attribute:: persistent
      

      

   .. attribute:: user
      

      

   .. attribute:: command
      

      

   .. attribute:: explicit
      

      

   .. attribute:: framework
      

      

   .. attribute:: collator
      

      

   .. attribute:: __slots__
      :annotation: = ['rank']

      

   .. method:: __eq__(self, other)



   .. method:: __lt__(self, other)



   .. method:: __str__(self)




.. data:: categories
   

   

.. py:class:: Uninitialized

   Bases: :class:`pyre.framework.Priority.Priority`

   Category for unspecified priorities; meant to be used as default values for arguments to
   functions

   .. attribute:: name
      :annotation: = uninitialized

      

   .. attribute:: category
      

      

   .. attribute:: __slots__
      :annotation: = []

      


.. py:class:: Defaults

   Bases: :class:`pyre.framework.Priority.Priority`

   Category for the priorities of the default values of traits, i.e. the values in the class
   declarations

   .. attribute:: name
      :annotation: = defaults

      

   .. attribute:: category
      

      

   .. attribute:: __slots__
      :annotation: = []

      


.. py:class:: Boot

   Bases: :class:`pyre.framework.Priority.Priority`

   Category for the priorities of values assigned while the framework is booting

   .. attribute:: name
      :annotation: = boot

      

   .. attribute:: category
      

      

   .. attribute:: __slots__
      :annotation: = []

      


.. py:class:: Package

   Bases: :class:`pyre.framework.Priority.Priority`

   Category for the priorities of values assigned while package configurations are being
   retrieved

   .. attribute:: name
      :annotation: = package

      

   .. attribute:: category
      

      

   .. attribute:: __slots__
      :annotation: = []

      


.. py:class:: Persistent

   Bases: :class:`pyre.framework.Priority.Priority`

   Category for the priorities of values retrieved from an application supplied persistent
   store where components record their configurations

   .. attribute:: name
      :annotation: = persistent

      

   .. attribute:: category
      

      

   .. attribute:: __slots__
      :annotation: = []

      


.. py:class:: User

   Bases: :class:`pyre.framework.Priority.Priority`

   Category for the priorities of values assigned during the processing of user configuration
   events

   .. attribute:: name
      :annotation: = user

      

   .. attribute:: category
      

      

   .. attribute:: __slots__
      :annotation: = []

      


.. py:class:: Command

   Bases: :class:`pyre.framework.Priority.Priority`

   Category for the priorities of values assigned during the processing of the command line

   .. attribute:: name
      :annotation: = command

      

   .. attribute:: category
      

      

   .. attribute:: __slots__
      :annotation: = []

      


.. py:class:: Explicit

   Bases: :class:`pyre.framework.Priority.Priority`

   Category for the priorities of values assigned explicitly by the user program

   .. attribute:: name
      :annotation: = explicit

      

   .. attribute:: category
      

      

   .. attribute:: __slots__
      :annotation: = []

      


.. py:class:: Framework

   Bases: :class:`pyre.framework.Priority.Priority`

   Category for the priorities of read-only values assigned by the framework

   .. attribute:: name
      :annotation: = framework

      

   .. attribute:: category
      

      

   .. attribute:: __slots__
      :annotation: = []

      


.. data:: uninitialized
   

   

.. data:: defaults
   

   

.. data:: boot
   

   

.. data:: package
   

   

.. data:: command
   

   

.. data:: user
   

   

.. data:: explicit
   

   

.. data:: framework
   

   

