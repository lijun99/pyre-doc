:mod:`pyre.shells.Director`
===========================

.. py:module:: pyre.shells.Director


Module Contents
---------------

.. py:class:: Director(name, bases, attributes, namespace=None, **kwds)

   Bases: :class:`pyre.actor`

   The metaclass of applications

   {Director} takes care of all the tasks necessary to register an application family with the
   framework

   .. method:: __call__(self, name=None, globalAliases=True, locator=None, **kwds)


      Instantiate one of my classes



