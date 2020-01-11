:mod:`cuda.Device`
==================

.. py:module:: cuda.Device


Module Contents
---------------

.. py:class:: Device

   The property sheet of a CUDA capable device

   .. attribute:: id
      

      

   .. attribute:: name
      :annotation: = 

      

   .. attribute:: capability
      :annotation: = []

      

   .. attribute:: driverVersion
      :annotation: = []

      

   .. attribute:: runtimeVersion
      :annotation: = []

      

   .. attribute:: computeMode
      :annotation: = 0

      

   .. attribute:: managedMemory
      :annotation: = False

      

   .. attribute:: unifiedAddressing
      :annotation: = False

      

   .. attribute:: processors
      :annotation: = 0

      

   .. attribute:: coresPerProcessor
      :annotation: = 0

      

   .. attribute:: globalMemory
      :annotation: = 0

      

   .. attribute:: constantMemory
      :annotation: = 0

      

   .. attribute:: sharedMemoryPerBlock
      :annotation: = 0

      

   .. attribute:: warp
      :annotation: = 0

      

   .. attribute:: maxThreadsPerBlock
      :annotation: = 0

      

   .. attribute:: maxThreadsPerProcessor
      :annotation: = 0

      

   .. attribute:: maxGrid
      :annotation: = []

      

   .. attribute:: maxThreadBlock
      :annotation: = []

      

   .. attribute:: _cublas_handle
      

      

   .. attribute:: _curand_generator
      

      

   .. attribute:: _cusolverdn_handle
      

      

   .. method:: initialize(self)


      Initialize device and its handles


   .. method:: cublas_handle(self)
      :property:


      Return (create if not exist) a cublas handle
      :return:


   .. method:: get_cublas_handle(self)



   .. method:: cusolverdn_handle(self)
      :property:



   .. method:: get_cusolverdn_handle(self)



   .. method:: curand_generator(self)
      :property:


      Get (create if not exist) the curand_generator attached to device
      :return:


   .. method:: get_curand_generator(self)



   .. method:: reset(self)


      Reset the current device


   .. method:: synchronize(self)


      Synchronize the current device


   .. method:: dump(self, indent='')


      Print information about this device



