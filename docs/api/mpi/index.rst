:mod:`mpi`
==========

.. py:module:: mpi


Submodules
----------
.. toctree::
   :titlesonly:
   :maxdepth: 1

   Cartesian/index.rst
   Communicator/index.rst
   Group/index.rst
   Launcher/index.rst
   Object/index.rst
   Port/index.rst
   Slurm/index.rst
   TrivialCommunicator/index.rst
   meta/index.rst


Package Contents
----------------

.. py:class:: world

   A trivial implementation of an MPI communicator

   .. attribute:: rank
      :annotation: = 0

      

   .. attribute:: size
      :annotation: = 1

      


.. data:: mpi
   

   

.. function:: init()

   Initialize the runtime

   We used to do this automatically, but that's not possible any more. The reason is that
   processes cannot fork/exec {mpirun} after they have called {MPI_Init}. Apparently, this has
   been discouraged always by {openmpi}, and it is explicitly prohibited with {openmpi-3.0}. So
   here we are...


.. function:: finalize()

   Shutdown mpi


.. data:: package
   

   

.. function:: copyright()

   Return the pyre copyright note


.. function:: license()

   Print the pyre license


.. function:: version()

   Return the pyre version


.. function:: credits()

   Print the acknowledgments


