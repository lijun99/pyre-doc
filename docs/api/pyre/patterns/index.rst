:mod:`pyre.patterns`
====================

.. py:module:: pyre.patterns

.. autoapi-nested-parse::

   This package contains functions and classes that encapsulate common usage patterns.



Submodules
----------
.. toctree::
   :titlesonly:
   :maxdepth: 1

   AbstractMetaclass/index.rst
   Accumulator/index.rst
   AttributeClassifier/index.rst
   CoFunctor/index.rst
   ExtentAware/index.rst
   Named/index.rst
   Observable/index.rst
   PathHash/index.rst
   Printer/index.rst
   Singleton/index.rst
   Tee/index.rst


Package Contents
----------------

.. py:class:: observable(**kwds)

   Provide notification support for classes that maintain dynamic associations with multiple
   clients.

   Observers, i.e. clients of the Observable, register event handlers that will be invoked to
   notify them whenever something interesting happens to the Observable. The nature of what is
   being observed is defined by Observable descendants and their managers. For example,
   instances of pyre.calc.Node are observable by the other nodes whose value depends on
   them. These dependents are notified of value changes and forced to refresh their value
   cache.

   The event handlers are callables that take the observable instance as their single
   argument.

   interface:
     addObserver: registers its callable argument with the list of handlers to invoke
     removeObserver: remove an event handler from the list of handlers to invoke
     notifyObservers: invoke the registered handlers in the order in which they were registered

   .. attribute:: observers
      

      

   .. method:: notifyObservers(self, **kwds)


      Notify all observers


   .. method:: addObserver(self, callback)


      Add {callback} to the set of observers


   .. method:: removeObserver(self, callback)


      Remove {callback} from the set of observers



.. function:: mean(iterable)

   Compute the mean value of the entries in {iterable}


.. function:: powerset(iterable)

   Compute the full power set, i.e. the set of all permutations, of the given iterable.
   For example:
       powerset([1,2,3]) --> () (1,) (2,) (3,) (1,2) (1,3) (2,3) (1,2,3)"
   Taken from the python itertools documentation


.. function:: vivify(levels=1, atom=dict)

   Builds a nested {defaultdict} with a fixed depth and a specified type at the deepest level.

   Adopted from (http://en.wikipedia.org/wiki/Autovivification)


.. function:: newPathHash(**kwds)

   Build a hashing functor for name hierarchies


.. py:class:: cofunctor(*args, **kwds)

   Converts a functor into a coroutine

   .. method:: send(self, value)


      Accept a value


   .. method:: throw(self, errorTp, error=None, traceback=None)


      Raise an exception


   .. method:: close(self)


      Shut things down


   .. method:: __next__(self)


      Advance



.. py:class:: accumulator(**kwds)

   Bases: :class:`pyre.patterns.CoFunctor.CoFunctor`

   A coroutine that accumulates data in a container

   .. method:: throw(self, errorTp, error=None, traceback=None)


      Handle exceptions


   .. method:: __call__(self)


      Store everything that comes in



.. py:class:: printer(format=None, **kwds)

   Bases: :class:`pyre.patterns.CoFunctor.CoFunctor`

   A coroutine that sends a textual representation of the values it receives to {stdout}

   .. method:: throw(self, errorTp, error=None, traceback=None)


      Handle exceptions


   .. method:: __call__(self)


      Store everything that comes in



.. py:class:: tee

   Bases: :class:`pyre.patterns.CoFunctor.CoFunctor`, :class:`list`

   A coroutine that accumulates data in a container

   .. method:: throw(self, errorTp, error=None, traceback=None)


      Raise an exception


   .. method:: close(self)


      Shut things down


   .. method:: __call__(self)


      Store everything that comes in



.. function:: coroutine(f)

   Decorator that automatically primes a coroutine


