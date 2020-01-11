:mod:`mpi.Slurm`
================

.. py:module:: mpi.Slurm


Module Contents
---------------

.. py:class:: Slurm

   Bases: :class:`mpi.Launcher.Launcher`

   Encapsulation of launching an MPI job using SLURM

   .. attribute:: sbatch
      

      

   .. attribute:: doc
      :annotation: = the path to the sbatch launcher

      

   .. attribute:: queue
      

      

   .. attribute:: doc
      :annotation: = the name of the queue that will receive this job

      

   .. attribute:: submit
      

      

   .. attribute:: doc
      :annotation: = if {True} invoke sbatch; otherwise just save the SLURM script in a file

      

   .. method:: spawn(self, application)


      Generate a {SLURM} script and submit a job



