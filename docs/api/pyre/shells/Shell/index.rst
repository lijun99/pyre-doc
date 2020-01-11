:mod:`pyre.shells.Shell`
========================

.. py:module:: pyre.shells.Shell


Module Contents
---------------

.. py:class:: Shell

   Bases: :class:`pyre.protocol`

   The protocol implemented by the pyre application hosting strategies

   .. attribute:: home
      

      

   .. attribute:: doc
      :annotation: = the process home directory

      

   .. attribute:: hosts
      

      

   .. attribute:: doc
      :annotation: = the number of hosts in the parallel machine

      

   .. attribute:: tasks
      

      

   .. attribute:: doc
      :annotation: = the number of tasks per host

      

   .. attribute:: gpus
      

      

   .. attribute:: doc
      :annotation: = the number of GPU coprocessors per task

      

   .. attribute:: model
      

      

   .. attribute:: doc
      :annotation: = the programming model

      

   .. method:: pyre_default(cls, **kwds)
      :classmethod:


      The default shell implementation


   .. method:: launch(self, application, *args, **kwds)


      Launch the application



