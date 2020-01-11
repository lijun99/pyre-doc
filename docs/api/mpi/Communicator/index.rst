:mod:`mpi.Communicator`
=======================

.. py:module:: mpi.Communicator


Module Contents
---------------

.. py:class:: Communicator(capsule, **kwds)

   Bases: :class:`mpi.Object.Object`

   An encapsulation of MPI communicators

   .. attribute:: rank
      :annotation: = 0

      

   .. attribute:: size
      :annotation: = 1

      

   .. attribute:: capsule
      

      

   .. method:: restrict(self, group)


      Build a new communicator with the process in {group}, which is expected to be a
      communicator group


   .. method:: include(self, processes)


      Build a new communicator with the processes in the iterable {processes} as its members


   .. method:: exclude(self, processes)


      Build a new communicator with all my processes except those in {processes}


   .. method:: cartesian(self, axes, periods, reorder=1)


      Build a cartesian communicator; see the MPI documentation for details


   .. method:: barrier(self)


      Establish a synchronization point: all processes in this communicator must call this
      method, and they all block until the last one makes the call


   .. method:: group(self)


      Build a group that contains all my processes


   .. method:: port(self, peer, tag=Port.tag)


      Establish a point-to-point communication conduit with {peer}; all messages sent through
      this port will be tagged with {tag}


   .. method:: bcast(self, item=None, source=0)


      Broadcast {item} from {source} to every task; only {source} has to pass an {item}


   .. method:: sum(self, item, destination=None)


      Perform a sum reduction of {item} using {exemplar} to deduce the type and deliver the
      result to the MPI task whose rank is given in {destination}
      If {destination} is not provided, deliver the results to all processes


   .. method:: product(self, item, destination=None)


      Perform a product reduction of {item}
      If {destination} is not provided, deliver the results to all processes


   .. method:: max(self, item, destination=None)


      Perform a max reduction of {item}
      If {destination} is not provided, deliver the results to all processes


   .. method:: min(self, item, destination=None)


      Perform a min reduction of {item}
      If {destination} is not provided, deliver the results to all processes



