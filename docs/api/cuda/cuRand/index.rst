:mod:`cuda.cuRand`
==================

.. py:module:: cuda.cuRand


Module Contents
---------------

.. py:class:: cuRand

   CURAND lib utitilies

   .. attribute:: CURAND_RNG_TEST
      :annotation: = [0]

      

   .. attribute:: CURAND_RNG_PSEUDO_DEFAULT
      :annotation: = 100

      

   .. attribute:: CURAND_RNG_PSEUDO_XORWOW
      :annotation: = 101

      

   .. attribute:: CURAND_RNG_PSEUDO_MRG32K3A
      :annotation: = 121

      

   .. attribute:: CURAND_RNG_PSEUDO_MTGP32
      :annotation: = 141

      

   .. attribute:: CURAND_RNG_PSEUDO_MT19937
      :annotation: = 142

      

   .. attribute:: CURAND_RNG_PSEUDO_PHILOX4_32_10
      :annotation: = 161

      

   .. attribute:: CURAND_RNG_QUASI_DEFAULT
      :annotation: = 200

      

   .. attribute:: CURAND_RNG_QUASI_SOBOL32
      :annotation: = 201

      

   .. attribute:: CURAND_RNG_QUASI_SCRAMBLED_SOBOL32
      :annotation: = 202

      

   .. attribute:: CURAND_RNG_QUASI_SOBOL64
      :annotation: = 203

      

   .. attribute:: CURAND_RNG_QUASI_SCRAMBLED_SOBOL64
      :annotation: = 204

      

   .. method:: create_generator(gentype=None, seed=None)


      allocate a curand generator 


   .. method:: set_seed(gen, seed)


      Set seed for curand generator


   .. method:: get_current_generator()


      Find the curand generator from current device


   .. method:: gaussian(gen=None, out=None, dtype='float64', loc=0, scale=1, size=1)


      generate Gaussian(Normal) distribution random numbers 


   .. method:: uniform(gen=None, out=None, dtype='float64', size=1)


      generate uniform distribution random numbers (0,1] 



