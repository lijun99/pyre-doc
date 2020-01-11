:mod:`pyre.nexus.Fork`
======================

.. py:module:: pyre.nexus.Fork


Module Contents
---------------

.. py:class:: Fork

   Bases: :class:`pyre.component`

   Create worker processes by cloning the current one

   .. method:: recruit(self, team, **kwds)


      Recruit members for the {team}


   .. method:: deploy(self, team, **kwds)


      Create a new {team} member using the {fork} system call


   .. method:: dismiss(self, team, crew, **kwds)


      The {team} manager has dismissed the given {member}



