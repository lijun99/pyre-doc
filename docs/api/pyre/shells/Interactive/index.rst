:mod:`pyre.shells.Interactive`
==============================

.. py:module:: pyre.shells.Interactive


Module Contents
---------------

.. py:class:: Interactive

   Bases: :class:`pyre.shells.Script.Script`

   A shell that invokes the main application behavior and then enters interactive mode

   .. method:: launch(self, application, *args, **kwds)


      Invoke the application behavior


   .. method:: pyre_interactiveSession(self, application=None, banner=None, context=None)


      Convert this session to an interactive one


   .. method:: pyre_enrich(self, tag)


      Attempt to provide a richer interactive experience



