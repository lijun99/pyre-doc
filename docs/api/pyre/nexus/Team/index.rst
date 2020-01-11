:mod:`pyre.nexus.Team`
======================

.. py:module:: pyre.nexus.Team


Module Contents
---------------

.. py:class:: Team

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



