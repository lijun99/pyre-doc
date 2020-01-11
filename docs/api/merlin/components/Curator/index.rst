:mod:`merlin.components.Curator`
================================

.. py:module:: merlin.components.Curator


Module Contents
---------------

.. py:class:: Curator

   Bases: :class:`merlin.component`

   The component that manages the project persistent store

   .. attribute:: projectURI
      

      

   .. attribute:: doc
      :annotation: = the location of the persistent project state

      

   .. method:: loadProject(self)


      Retrieve the project configuration information from the archive


   .. method:: saveProject(self, project)


      Save the given project configuration to the archive


   .. method:: saveAsset(self, asset)


      Save the given asset to the archive


   .. method:: load(self, node)


      Retrieve an object from the merlin file identified by {tag}


   .. method:: save(self, tag, item)


      Pickle {item} into the merlin file indicated by {tag}



