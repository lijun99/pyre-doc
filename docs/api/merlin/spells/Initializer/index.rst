:mod:`merlin.spells.Initializer`
================================

.. py:module:: merlin.spells.Initializer


Module Contents
---------------

.. py:class:: Initializer

   Bases: :class:`merlin.spell`

   Create a new merlin project rooted at the given directory

   .. attribute:: project
      

      

   .. attribute:: doc
      :annotation: = the name of the project

      

   .. attribute:: createPrefix
      

      

   .. attribute:: doc
      :annotation: = create all directories leading up to the specified target

      

   .. attribute:: force
      

      

   .. attribute:: doc
      :annotation: = initialize the target folder regardless of whether is it already part of a project

      

   .. method:: main(self, plexus, argv)


      Make {folder} the root of a new merlin project. The target {folder} is given as an
      optional command line argument, and defaults to the current directory. Issue an error
      message if {folder} is already a merlin project.



