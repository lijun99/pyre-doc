:mod:`merlin.components.Merlin`
===============================

.. py:module:: merlin.components.Merlin


Module Contents
---------------

.. py:class:: Merlin(name, **kwds)

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



