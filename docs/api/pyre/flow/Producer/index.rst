:mod:`pyre.flow.Producer`
=========================

.. py:module:: pyre.flow.Producer


Module Contents
---------------

.. py:class:: Producer

   Bases: :class:`pyre.protocol`

   The requirements that all factories must implement

   .. method:: make(self, **kwds)


      Build all products


   .. method:: plan(self, **kwds)


      Describe what needs to get to done to make the products



