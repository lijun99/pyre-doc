:mod:`pyre.nexus.Asynchronous`
==============================

.. py:module:: pyre.nexus.Asynchronous


Module Contents
---------------

.. py:class:: Asynchronous

   Bases: :class:`pyre.protocol`

   A protocol that specifies the two ingredients necessary for building event driven
   applications

   .. attribute:: marshaler
      

      

   .. attribute:: doc
      :annotation: = the serializer that enables the transmission of objects among peers

      

   .. attribute:: dispatcher
      

      

   .. attribute:: doc
      :annotation: = the manager of the event loop

      

   .. method:: run(self)


      Start processing requests


   .. method:: prepare(self)


      Carry out any necessary start up steps


   .. method:: watch(self)


      Activate my event loop


   .. method:: shutdown(self)


      Signal my event loop to stop processing events


   .. method:: shutdown(self)


      Shut down and exit gracefully



