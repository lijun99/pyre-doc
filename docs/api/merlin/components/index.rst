:mod:`merlin.components`
========================

.. py:module:: merlin.components


Submodules
----------
.. toctree::
   :titlesonly:
   :maxdepth: 1

   Action/index.rst
   Component/index.rst
   Curator/index.rst
   Dashboard/index.rst
   Merlin/index.rst
   PythonClassifier/index.rst
   Spell/index.rst
   Spellbook/index.rst
   exceptions/index.rst


Package Contents
----------------

.. py:class:: action

   Bases: :class:`pyre.action`, :class:`merlin.components.Dashboard.Dashboard`

   Protocol declaration for merlin spells


.. py:class:: spell

   Bases: :class:`pyre.panel()`, :class:`merlin.components.Dashboard.Dashboard`

   Base class for merlin spell implementations

   .. method:: vfs(self)
      :property:


      Access to the fileserver



.. py:class:: component

   Bases: :class:`pyre.component`, :class:`merlin.components.Dashboard.Dashboard`

   Minor merlin specific embellishment of the {pyre.component} base class

   .. method:: vfs(self)
      :property:


      Convenient access to the application fileserver



.. py:class:: dashboard

   Resting place for the {merlin} singletons

   .. attribute:: merlin
      

      


.. py:class:: merlin(name, **kwds)

   Bases: :class:`pyre.plexus`

   The merlin executive and application wrapper

   .. attribute:: pyre_namespace
      :annotation: = merlin

      

   .. attribute:: METAFOLDER
      :annotation: = .merlin

      

   .. attribute:: PATH
      :annotation: = ['vfs:/merlin/project', 'vfs:/merlin/user', 'vfs:/merlin/system']

      

   .. method:: searchpath(self)
      :property:


      Build a list of unique package names from my ancestry in mro order


   .. method:: help(self, **kwds)


      Hook for the application help system


   .. method:: newProject(self, name)


      Create a new project description object


   .. method:: pyre_mountApplicationFolders(self, pfs, prefix)


      Build my private filesystem


   .. method:: pyre_newRepertoir(self)


      Build my spell manager


   .. method:: locateProjectRoot(self, folder=None)


      Check whether {folder} is contained within a {merlin} project



