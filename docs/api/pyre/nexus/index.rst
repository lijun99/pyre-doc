:mod:`pyre.nexus`
=================

.. py:module:: pyre.nexus


Submodules
----------
.. toctree::
   :titlesonly:
   :maxdepth: 1

   Asynchronous/index.rst
   Crew/index.rst
   CrewStatus/index.rst
   Fork/index.rst
   Nexus/index.rst
   Node/index.rst
   Peer/index.rst
   Pool/index.rst
   Recruiter/index.rst
   Server/index.rst
   Service/index.rst
   Task/index.rst
   TaskStatus/index.rst
   Team/index.rst
   exceptions/index.rst


Package Contents
----------------

.. py:class:: nexus

   Bases: :class:`pyre.nexus.Asynchronous.Asynchronous`

   Protocol definition for components that enable applications to interact over the network

   .. method:: pyre_default(cls, **kwds)
      :classmethod:


      The default implementation of the {Nexus} protocol



.. py:class:: service

   Bases: :class:`pyre.protocol`

   Protocol definition for components that handle events in communication channels

   .. method:: pyre_default(cls, **kwds)
      :classmethod:


      The suggested implementation of the {Service} protocol


   .. method:: activate(self, application, dispatcher)


      Prepare to start receiving information from the network


   .. method:: acknowledge(self, dispatcher, channel)


      A peer has attempted to establish a connection


   .. method:: validate(self, channel, address)


      Examine the peer {address} and determine whether to continue the conversation


   .. method:: connect(self, dispatcher, channel, address)


      Prepare to start accepting requests from a new peer


   .. method:: process(self, dispatcher, channel)


      Start or continue a conversation with a peer over {channel}


   .. method:: shutdown(self)


      Clean up and shutdown



.. py:class:: node(**kwds)

   Bases: :class:`pyre.nexus.Peer.Peer`

   .. attribute:: services
      

      

   .. attribute:: doc
      :annotation: = the table of available services

      

   .. attribute:: application
      

      

   .. method:: prepare(self, application)


      Get ready to listen for incoming connections


   .. method:: shutdown(self)


      Shut everything down and exit gracefully


   .. method:: reload(self)


      Reload the nodal configuration for a distributed application


   .. method:: signal(self, signal, frame)


      An adaptor that dispatches {signal} to the registered handler


   .. method:: newSignalIndex(self)


      By default, nodes register handlers for process termination and configuration reload


   .. method:: registerSignalHandlers(self)


      By default, nodes register handlers for process termination and configuration reload



.. py:class:: server

   Bases: :class:`pyre.component`

   The base class for network servers

   .. attribute:: address
      

      

   .. attribute:: application
      

      

   .. attribute:: dispatcher
      

      

   .. method:: activate(self, application, dispatcher)


      Grab a port and register it with the event dispatcher


   .. method:: acknowledge(self, channel)


      A peer has attempted to establish a connection


   .. method:: validate(self, channel, address)


      Examine the peer {address} and determine whether to continue the conversation


   .. method:: connect(self, channel, address)


      Prepare to start accepting requests from peers


   .. method:: process(self, channel)


      Say something to the peer


   .. method:: shutdown(self)


      Clean up and shutdown



.. py:class:: task

   Base class for functors that are part of an application data model

   .. method:: execute(self, **kwds)


      The body of the functor


   .. method:: __call__(self, **kwds)




.. py:class:: taskcodes

   Bases: :class:`enum.Enum`

   Indicators used by tasks to describe what happened during their execution

   .. attribute:: completed
      :annotation: = 0

      

   .. attribute:: failed
      :annotation: = 1

      

   .. attribute:: aborted
      :annotation: = 2

      

   .. attribute:: damaged
      :annotation: = 3

      


.. py:class:: crewcodes

   Bases: :class:`enum.Enum`

   Indicators used by crew members to describe what happened during the execution of the most
   recent task that was assigned to them

   .. attribute:: healthy
      :annotation: = 0

      

   .. attribute:: damaged
      :annotation: = 1

      


.. py:class:: team

   Bases: :class:`pyre.protocol`

   The specification for a process collective that coöperate to carry out a work plan

   .. attribute:: size
      

      

   .. attribute:: doc
      :annotation: = the number of team members to recruit

      

   .. attribute:: recruiter
      

      

   .. attribute:: doc
      :annotation: = the strategy for recruiting team members

      

   .. method:: assemble(self, workplan, **kwds)


      Recruit a team to execute the set of tasks in my {workplan}


   .. method:: vacancies(self)


      Compute how may recruits are needed to take the team to full strength


   .. method:: pyre_default(cls, **kwds)
      :classmethod:


      The default {Team} implementation



.. py:class:: recruiter

   Bases: :class:`pyre.protocol`

   The protocol of resource allocation strategies

   .. method:: recruit(self, team, **kwds)


      Recruit members for the {team}


   .. method:: deploy(self, team, **kwds)


      Create a new {team} member


   .. method:: dismiss(self, team, member, **kwds)


      The {team} manager has dismissed the given {member}


   .. method:: pyre_default(cls, **kwds)
      :classmethod:


      The default {Recruiter} implementation



.. py:class:: asynchronous

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



.. function:: fork()

   Use fork as the team member recruitment strategy


.. function:: peer()

   The base class for components that provide an application with its event loop


.. function:: pool()

   The manager of a team that execute a workplan concurrently


