:mod:`pyre.tracking`
====================

.. py:module:: pyre.tracking


Submodules
----------
.. toctree::
   :titlesonly:
   :maxdepth: 1

   Chain/index.rst
   Command/index.rst
   File/index.rst
   FileRegion/index.rst
   NameLookup/index.rst
   Script/index.rst
   Simple/index.rst
   Tracker/index.rst


Package Contents
----------------

.. py:class:: chain(this, next)

   A locator that ties together two others in order to express that something in {next}
   caused {this} to be recorded

   .. attribute:: __slots__
      :annotation: = ['this', 'next']

      

   .. method:: __str__(self)




.. py:class:: command(arg)

   A locator that records the position of a command line argument

   .. attribute:: source
      :annotation: = from the command line argument {!r}

      

   .. attribute:: __slots__
      :annotation: = ['arg']

      

   .. method:: __str__(self)




.. py:class:: file(source, line=None, column=None)

   A locator that records a position within a file

   .. attribute:: __slots__
      :annotation: = ['source', 'line', 'column']

      

   .. method:: __str__(self)




.. py:class:: region(start, end)

   A locator that records information about a region of a file

   .. attribute:: __slots__
      :annotation: = ['start', 'end']

      

   .. method:: __str__(self)




.. py:class:: lookup(description, key)

   A locator that records a simple named source with no further details

   .. attribute:: __slots__
      :annotation: = ['key', 'description']

      

   .. method:: __str__(self)




.. py:class:: script(source, line=None, function=None)

   A locator that records information relevant to python scripts. This information is
   typically extracted from stack traces so it contains whatever can be harvested by
   introspection

   .. attribute:: __slots__
      :annotation: = ['source', 'line', 'function']

      

   .. method:: __str__(self)




.. py:class:: simple(source)

   A locator that records a simple named source with no further details

   .. attribute:: __slots__
      :annotation: = ['source']

      

   .. method:: __str__(self)




.. py:class:: tracker(**kwds)

   Record the values a key has taken

   .. method:: getHistory(self, key)


      Retrieve the historical record associated with a particular {key}


   .. method:: track(self, key, node)


      Add {value} to the history of {key}



.. data:: callerStackDepth
   :annotation: = 2

   

.. function:: unknown()


.. function:: here(level=0)

   Build a locator that records the caller's location

   The parameter {level} specifies the level above the caller that is to be used as the
   originating location. The default, {level}=0, indicates to use the caller's location;
   setting {level} to 1 will use the caller's caller's location, and so on.


