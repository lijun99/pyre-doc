:mod:`merlin.components.PythonClassifier`
=========================================

.. py:module:: merlin.components.PythonClassifier


Module Contents
---------------

.. py:class:: PythonClassifier

   Bases: :class:`merlin.component`

   An asset classifier that recognizes modules, packages and extensions

   .. attribute:: INIT
      

      

   .. method:: classify(self, root, node)


      Explore {node}, assuming it is an instance of a {pyre.filesystem.Node} subclass,
      looking for assets



