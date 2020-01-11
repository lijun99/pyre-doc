:mod:`pyre.nexus.Pool`
======================

.. py:module:: pyre.nexus.Pool


Module Contents
---------------

.. py:class:: Pool(crew=None, **kwds)

   Bases: :class:`pyre.nexus.Peer.Peer`

   A process collective that coöperate to carry out a work plan

   .. attribute:: size
      

      

   .. attribute:: doc
      :annotation: = the number of crew members to recruit

      

   .. attribute:: recruiter
      

      

   .. attribute:: doc
      :annotation: = the strategy for recruiting crew members

      

   .. attribute:: active
      

      

   .. attribute:: retired
      

      

   .. method:: assemble(self, workplan, **kwds)


      Assemble a team to execute the set of tasks in my {workplan}


   .. method:: vacancies(self)


      Compute how may recruits are needed to take the team to full strength


   .. method:: recruit(self, **kwds)


      Assemble the team


   .. method:: activate(self, crew)


      Add the given {crew} member to the scheduling queue


   .. method:: schedule(self, crew)


      Add the given {crew} member to the execution schedule


   .. method:: submit(self, channel, crew, **kwds)


      A crew member has reported ready to accept tasks


   .. method:: dismiss(self, crew)


      Dismiss the {crew} member from the team



