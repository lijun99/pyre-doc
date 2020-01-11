:mod:`pyre.xml.Ignorable`
=========================

.. py:module:: pyre.xml.Ignorable


Module Contents
---------------

.. py:class:: Ignorable(**kwds)

   Bases: :class:`pyre.xml.Node.Node`

   Handler that ignores the subtree anchored at its tag

   .. method:: newNode(self, **kwds)


      Invoked when a new opening tag is encountered in my subtree


   .. method:: newQNode(self, **kwds)


      Invoked when a new namespace qualified opening tag is encountered in my subtree


   .. method:: notify(self, **kwds)


      Invoked when a closing tag in encountered in my subtree



