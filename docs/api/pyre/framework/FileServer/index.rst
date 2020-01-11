:mod:`pyre.framework.FileServer`
================================

.. py:module:: pyre.framework.FileServer


Module Contents
---------------

.. py:class:: FileServer(executive=None, **kwds)

   Bases: :class:`pyre.filesystem.Filesystem.Filesystem`

   The manager of the virtual filesystem

   Instances of {FileServer} manage hierarchical namespaces implemented as a virtual
   filesystem. The contents of these namespaces are retrieved using URIs, and can be arbitrary
   objects, although they are typically either local or remote files.

   The framework uses a {FileServer} instance to decouple the logical names of resources from
   their physical locations at runtime. For example, during the bootstrapping process the
   framework looks for user preferences for pyre applications. On Unix like machines, these
   are stored in '~/.pyre' and its subfolders. The entire hierarchy is mounted in the virtual
   filesystem under '/-/user'. This has the following advantages:

   * applications can navigate through the contents of '/-/user' as if it were an actual
     filesystem

   * configuration settings that require references to entries in '/_/user' can now be
     expressed portably, since there is no need to hardwire actual paths

   Applications are encouraged to lay out their own custom namespaces. The application
   developer can refer to resources through their standardized logical names, whereas the user
   is free to provide the mapping that reflects their physical location at runtime.

   .. attribute:: DOT_PYRE
      

      

   .. attribute:: USER_DIR
      

      

   .. attribute:: STARTUP_DIR
      

      

   .. attribute:: PACKAGES_DIR
      

      

   .. method:: systemFolders(self)
      :property:


      Return the sequence of uris of the {pyre} system folders


   .. method:: open(self, uri, **kwds)


      Convert {uri} into an input stream


   .. method:: local(self, root, **kwds)


      Build a local filesystem


   .. method:: virtual(self, **kwds)


      Build a virtual filesystem


   .. method:: initializeNamespace(self)


      Construct the initial layout of my virtual filesystem


   .. method:: registerPackage(self, package)


      Make the package configuration folder accessible in the virtual filesystem


   .. method:: retrieveFilesystem(self, root, levels=1)


      Retrieve {root} if it is an already mounted filesystem; if not, mount it and return it



