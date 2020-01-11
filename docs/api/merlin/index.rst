:mod:`merlin`
=============

.. py:module:: merlin

.. autoapi-nested-parse::

   merlin is a package intended as a replacement to {make}



Subpackages
-----------
.. toctree::
   :titlesonly:
   :maxdepth: 3

   assets/index.rst
   components/index.rst
   schema/index.rst
   spells/index.rst


Package Contents
----------------

.. function:: main()

   This is the main entry point in the package. It is invoked by the {merlin} script.  Its job
   is to boot pyre, examine the command line to deduce which actor the user would like to
   invoke, instantiate it, and call its main entry point with the supplied command line
   arguments.

   There are other possible ways to invoke merlin. See the package documentation.


.. function:: credits()

   Print the acknowledgments


.. function:: copyright()

   Return the merlin copyright note


.. function:: license()

   Print the merlin license


.. function:: version()

   Return the merlin version


.. function:: boot()


.. py:class:: component

   Bases: :class:`pyre.component`, :class:`merlin.components.Dashboard.Dashboard`

   Minor merlin specific embellishment of the {pyre.component} base class

   .. method:: vfs(self)
      :property:


      Convenient access to the application fileserver



.. py:class:: action

   Bases: :class:`pyre.action`, :class:`merlin.components.Dashboard.Dashboard`

   Protocol declaration for merlin spells


.. py:class:: spell

   Bases: :class:`pyre.panel()`, :class:`merlin.components.Dashboard.Dashboard`

   Base class for merlin spell implementations

   .. method:: vfs(self)
      :property:


      Access to the fileserver



.. function:: error(message)

   Generate an error message


.. function:: warning(message)

   Generate a warning


.. function:: info(message)

   Generate an informational message


.. data:: package
   

   

.. data:: home
   

   

.. data:: prefix
   

   

.. data:: defaults
   

   

.. data:: merlin
   

   

