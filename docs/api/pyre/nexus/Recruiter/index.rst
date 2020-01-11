:mod:`pyre.nexus.Recruiter`
===========================

.. py:module:: pyre.nexus.Recruiter


Module Contents
---------------

.. py:class:: Recruiter

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



