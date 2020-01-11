:mod:`pyre.nexus.Peer`
======================

.. py:module:: pyre.nexus.Peer


Module Contents
---------------

.. py:class:: Peer(name=None, timer=None, **kwds)

   Bases: :class:`pyre.component`

   A component base class that supplies the two ingredients necessary for building event
   driven applications

   .. attribute:: marshaler
      

      

   .. attribute:: doc
      :annotation: = the serializer that enables the transmission of objects among peers

      

   .. attribute:: dispatcher
      

      

   .. attribute:: doc
      :annotation: = the manager of the event loop

      

   .. attribute:: timer
      

      

   .. method:: run(self)


      Start processing requests


   .. method:: prepare(self)


      Carry out any necessary start up steps


   .. method:: watch(self)


      Activate my event loop


   .. method:: shutdown(self)


      Shut the peer down and exit gracefully


   .. method:: stop(self)


      Signal my event loop to stop processing events



