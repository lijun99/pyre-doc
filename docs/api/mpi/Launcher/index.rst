:mod:`mpi.Launcher`
===================

.. py:module:: mpi.Launcher


Module Contents
---------------

.. py:class:: Launcher

   Bases: :class:`pyre.shells.Script.Script`

   Encapsulation of launching an MPI job using {mpirun}

   .. attribute:: hosts
      

      

   .. attribute:: doc
      :annotation: = the number of hosts in the parallel machine

      

   .. attribute:: tasks
      

      

   .. attribute:: default
      

      

   .. attribute:: doc
      :annotation: = the number of mpi tasks per host; defaults to the number of cores

      

   .. attribute:: hostfile
      

      

   .. attribute:: doc
      :annotation: = the name of the file that describes the machine

      

   .. attribute:: auto
      

      

   .. attribute:: doc
      :annotation: = set to {True} to re-launch this script under {mpirun}

      

   .. attribute:: mpi
      

      

   .. attribute:: doc
      :annotation: = the mpi runtime of choice

      

   .. attribute:: extra
      

      

   .. attribute:: doc
      :annotation: = extra arguments to pass to {mpirun}

      

   .. attribute:: model
      

      

   .. attribute:: doc
      :annotation: = the programming model

      

   .. attribute:: world
      

      

   .. method:: launch(self, application, *args, **kwds)


      Launch {application} as a collection of mpi tasks


   .. method:: parallel(self, *args, **kwds)


      Called after the parallel machine has been built and it is time to invoke the user's
      code in every node


   .. method:: spawn(self, application, *args, **kwds)


      Invoke {mpirun} with the correct arguments to create the  parallel machine


   .. method:: buildCommandLine(self)


      Construct the mpirun command line



