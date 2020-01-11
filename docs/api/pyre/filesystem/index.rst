:mod:`pyre.filesystem`
======================

.. py:module:: pyre.filesystem


Submodules
----------
.. toctree::
   :titlesonly:
   :maxdepth: 1

   BlockDevice/index.rst
   CharacterDevice/index.rst
   Directory/index.rst
   Explorer/index.rst
   File/index.rst
   Filesystem/index.rst
   Finder/index.rst
   Folder/index.rst
   HDF5/index.rst
   Info/index.rst
   InfoFile/index.rst
   InfoFolder/index.rst
   InfoStat/index.rst
   InfoZip/index.rst
   InfoZipFile/index.rst
   InfoZipFolder/index.rst
   Link/index.rst
   Local/index.rst
   Naked/index.rst
   NamedPipe/index.rst
   Node/index.rst
   Recognizer/index.rst
   SimpleExplorer/index.rst
   Socket/index.rst
   Stat/index.rst
   TreeExplorer/index.rst
   Walker/index.rst
   Zip/index.rst
   exceptions/index.rst


Package Contents
----------------

.. function:: virtual(**kwds)

   Build a virtual filesystem


.. function:: local(root, listdir=None, recognizer=None, **kwds)

   Build a local filesystem, i.e. one that encapsulates the contents of a filesystem that is
   mounted on the machine that hosts this process.

   parameters:
       {root}: the directory to use as the root of the new filesystem
       {listdir}: the mechanism that lists the contents of directories
       {recognizer}: the mechanism that identifies the types of files


.. function:: zip(root, **kwds)

   Attempt to build a zip filesystem out of {root}, which is expected to be a zip archive


.. function:: naked(**kwds)

   Build a naked node, i.e. a node that is a trivial wrapper around a file in the local
   filesystem. Useful for quick and dirty mounting of specific files without having to build a
   local filesystem out of the folder that contains them


.. function:: finder(**kwds)

   Build an explorer that traverses the contents of filesystems and returns ({node}, {name})
   pairs that match an optional {pattern}


.. function:: treeExplorer(**kwds)

   Build an explorer that creates a report of filesystem contents formatted like a tree


.. function:: simpleExplorer(**kwds)

   Build an explorer that creates a simple report of filesystem contents


.. function:: stat()

   Build a recognizer of the contents of local filesystems based on {os.stat}


.. function:: walker()

   Build an object that can list the contents of locally mounted folders


.. py:exception:: MountPointError(error, **kwds)

   Bases: :class:`pyre.filesystem.exceptions.GenericError`

   Exception generated when the root of a filesystem is invalid

   .. attribute:: description
      :annotation: = error while mounting '{0.uri}': {0.error}

      


.. data:: _metaclass_Node
   

   

.. function:: debug()

   Support for debugging the filesystem package


