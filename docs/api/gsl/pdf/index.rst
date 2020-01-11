:mod:`gsl.pdf`
==============

.. py:module:: gsl.pdf


Module Contents
---------------

.. py:class:: uniform(support, rng, **kwds)

   Encapsulation of the uniform probability distribution

   .. attribute:: support
      

      

   .. method:: sample(self)


      Sample the uniform distribution using a random value from {rng}


   .. method:: density(self, x)


      Compute the probability density of the uniform distribution at {x}


   .. method:: vector(self, vector)


      Fill {vector} with random values


   .. method:: matrix(self, matrix)


      Fill {matrix} with random values



.. py:class:: uniform_pos(rng, **kwds)

   Encapsulation of the positive uniform probability distribution

   .. method:: sample(self)


      Sample the uniform distribution using a random value from {rng}


   .. method:: density(self, x)


      Compute the probability density of the uniform distribution at {x}


   .. method:: vector(self, vector)


      Fill {vector} with random values


   .. method:: matrix(self, matrix)


      Fill {matrix} with random values



.. py:class:: gaussian(mean, sigma, rng, **kwds)

   Encapsulation of the gaussian probability distribution

   .. attribute:: mean
      :annotation: = 0.0

      

   .. attribute:: sigma
      

      

   .. method:: sample(self)


      Sample the gaussian distribution using a random value from {rng}


   .. method:: density(self, x)


      Compute the probability density of the gaussian distribution at {x}


   .. method:: vector(self, vector)


      Fill {vector} with random values


   .. method:: matrix(self, matrix)


      Fill {matrix} with random values



.. py:class:: ugaussian(rng, **kwds)

   Encapsulation of the unit gaussian probability distribution

   .. method:: sample(self)


      Sample the gaussian distribution using a random value from {rng}


   .. method:: density(self, x)


      Compute the probability density of the gaussian distribution at {x}


   .. method:: vector(self, vector)


      Fill {vector} with random values


   .. method:: matrix(self, matrix)


      Fill {matrix} with random values



.. py:class:: dirichlet(alpha, rng, **kwds)

   Encapsulation of the dirichlet probability distribution

   .. method:: vector(self, vector)


      Fill {vector} with random values


   .. method:: matrix(self, matrix)


      Fill {matrix} with random values



