:mod:`pyre.shells.Executive`
============================

.. py:module:: pyre.shells.Executive


Module Contents
---------------

.. py:class:: Executive

   Bases: :class:`pyre.component`

   The base class for hosting strategies

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

      

   .. method:: host(self)
      :property:


      Encapsulation of what is known about the runtime environment


   .. method:: launch(self, application, *args, **kwds)
      :abstractmethod:


      Invoke the application behavior



