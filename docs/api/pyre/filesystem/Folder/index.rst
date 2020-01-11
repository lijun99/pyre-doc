:mod:`pyre.filesystem.Folder`
=============================

.. py:module:: pyre.filesystem.Folder


Module Contents
---------------

.. py:class:: Folder(**kwds)

   Bases: :class:`pyre.filesystem.Node.Node`

   The base class for filesystem entries that are containers of other entries

   {Node} and {Folder} are the leaf and container types for the composite that enables the
   representation of the hierarchical structure of filesystems.

   .. attribute:: isFolder
      :annotation: = True

      

   .. method:: open(self)


      Return an iterable over my contents


   .. method:: mkdir(self, name, parents=True, exist_ok=True)



   .. method:: remove(self, node, name=None, **kwds)


      Remove {node} from my contents and its filesystem


   .. method:: write(self, name, contents, mode='w')


      Create a file with the given {name} and {contents}


   .. method:: find(self, pattern)


      Generate pairs ({node}, {name}) that match the given pattern

      By default, {find} will create a generator that visits the entire contents of the tree
      rooted at this folder. In order to restrict the set of matching names, provide a
      regular expression as the optional argument {pattern}


   .. method:: discover(self, **kwds)


      Fill my contents by querying whatever external resource my filesystem represents


   .. method:: mount(self, uri, filesystem)


      Make the root of {filesystem} available as {uri} within my filesystem


   .. method:: node(self)


      Build a new node within my filesystem


   .. method:: folder(self)


      Build a new folder within my filesystem


   .. method:: path(*args)
      :staticmethod:


      Assemble {args} into a path


   .. method:: __iter__(self)


      Return an iterator over my {contents}


   .. method:: __getitem__(self, uri)


      Retrieve a node given its {uri} as the subscript


   .. method:: __setitem__(self, uri, node)


      Attach {node} at {uri}


   .. method:: __contains__(self, uri)


      Check whether {uri} is one of my children


   .. method:: _retrieve(self, uri)


      Locate the entry with address {uri}


   .. method:: _insert(self, node, uri, metadata=None)


      Attach {node} at the address {uri}, creating all necessary intermediate folders.



