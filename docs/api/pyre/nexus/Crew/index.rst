:mod:`pyre.nexus.Crew`
======================

.. py:module:: pyre.nexus.Crew


Module Contents
---------------

.. py:class:: Crew(pid, channel, **kwds)

   Bases: :class:`pyre.nexus.Peer.Peer`

   The base facilitator of asynchronous task execution in foreign processes, and one of the
   building blocks of process based concurrency in pyre.

   Crew members are typically instantiated by a {recruiter} in matching pairs that are
   connected to each other via bidirectional {channels}. One member of the pair participates
   in the event logic of the host application; this instance is referred to as the team side
   crew member. The other is hosted by a remote pyre {shell} with its own event loop, and is
   referred to as the worker side. Making the worker side functional typically involves
   spinning up a new process, but this considered a {recruiter} implementation detail. The
   pair of crew instances are responsible only for the babysitting of the task execution.

   The team side crew member acts as a proxy for the worker side. The host application
   schedules the execution of a {task} by invoking the team side interface. The crew instance
   serializes the task and sends it off to its remote twin for execution, monitors progress,
   and reports the task result back to the host application.

   .. method:: join(self, team)


      Join a team

      This is invoked by my recruiter on the team side and it is part of team assembly. The
      intent is to make crew members available to the team after they have reported ready to
      receive tasks for execution


   .. method:: activate(self, channel, team)


      My worker twin is reporting ready to work

      N.B.: this is an event handler; careful with its return value


   .. method:: execute(self, team, task)


      Send my twin the {task} to be executed


   .. method:: assess(self, channel, team, task, **kwds)


      Harvest the task completion status


   .. method:: dismissed(self)


      My team manager has dismissed me


   .. method:: reportRecoverableError(self, team, task, error)


      Report a task failure that can be reasonably expected to be temporary


   .. method:: reportUnrecoverableError(self, team, task, error)


      Report a permanent task failure


   .. method:: register(self)


      Initialize the worker side


   .. method:: checkin(self, channel)


      Send my team registration now that my communication channel is open


   .. method:: perform(self, channel, **kwds)


      A notification has arrived that indicates there is a task waiting to be executed


   .. method:: engage(self, task, **kwds)


      Carry out the task


   .. method:: report(self, channel, crewstatus, taskstatus, result, **kwds)


      Post the task completion {report}


   .. method:: resign(self)




