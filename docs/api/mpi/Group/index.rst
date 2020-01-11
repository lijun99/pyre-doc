:mod:`mpi.Group`
================

.. py:module:: mpi.Group


Module Contents
---------------

.. py:class:: Group(capsule, **kwds)

   Bases: :class:`mpi.Object.Object`

   Encapsulation of MPI communicator groups

   .. attribute:: undefined
      

      

   .. attribute:: rank
      :annotation: = 0

      

   .. attribute:: size
      :annotation: = 0

      

   .. attribute:: capsule
      

      

   .. method:: isEmpty(self)


      Check whether i am an empty group


   .. method:: include(self, included)


      Build a group out of the processes in {included}


   .. method:: exclude(self, excluded)


      Build a group out of all processes except those in {excluded}


   .. method:: union(self, g)


      Build a new group whose processes are the union of mine and {g}'s


   .. method:: intersection(self, g)


      Build a new group whose processes are the intersection of mine and {g}'s


   .. method:: difference(self, g)


      Build a new group whose processes are the difference of mine and {g}'s



