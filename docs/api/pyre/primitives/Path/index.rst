:mod:`pyre.primitives.Path`
===========================

.. py:module:: pyre.primitives.Path


Module Contents
---------------

.. function:: _unaryDispatch(f)

   Wrapper for functions that require the string representation of path objects


.. py:class:: Path

   Bases: :class:`tuple`

   A representation of a path

   .. attribute:: _CWD
      :annotation: = .

      

   .. attribute:: _SEP
      :annotation: = /

      

   .. attribute:: root
      

      

   .. attribute:: chdir
      

      

   .. attribute:: chmod
      

      

   .. attribute:: lstat
      

      

   .. attribute:: stat
      

      

   .. attribute:: open
      

      

   .. attribute:: rmdir
      

      

   .. attribute:: unlink
      

      

   .. attribute:: __fspath__
      

      

   .. method:: parts(self)
      :property:


      Build an iterator over my components


   .. method:: names(self)
      :property:


      Build an iterator over the names of my components, skipping the root marker, if present


   .. method:: anchor(self)
      :property:


      Return the representation of the root of the path, if present


   .. method:: parents(self)
      :property:


      Generate a sequence of the logical ancestors of the path


   .. method:: crumbs(self)
      :property:


      Generate a sequence of paths from here to the root


   .. method:: parent(self)
      :property:


      Build a path that is my logical ancestor

      Note that this is purely a lexical operation and is not guaranteed to yield correct
      results unless this path has been fully resolved


   .. method:: name(self)
      :property:


      Return the final path component


   .. method:: path(self)
      :property:


      Return a string representing the full path


   .. method:: suffix(self)
      :property:


      The file extension of the final path component


   .. method:: suffixes(self)
      :property:


      Return an iterable over the extensions in name


   .. method:: stem(self)
      :property:


      The final path component without the last suffix


   .. method:: contents(self)
      :property:


      Generate a sequence of my contents


   .. method:: as_posix(self)


      Return a POSIX compliant representation


   .. method:: as_uri(self)


      Return a POSIX compliant representation


   .. method:: isAbsolute(self)


      Check whether the path is absolute or not


   .. method:: isReserved(self)


      Check whether the path is reserved or not


   .. method:: join(self, *others)


      Combine me with {others} and make a new path


   .. method:: relativeTo(self, other)


      Find a {path} such that {other} / {path} == {self}


   .. method:: withName(self, name)


      Build a new path with my name replaced by {name}


   .. method:: withSuffix(self, suffix=None)


      Build a new path with my suffix replaced by {suffix}


   .. method:: cwd(cls)
      :classmethod:


      Build a path that points to the current working directory


   .. method:: home(cls, user='')
      :classmethod:


      Build a path that points to the {user}'s home directory


   .. method:: resolve(self)


      Build an equivalent absolute normalized path that is free of symbolic links


   .. method:: expanduser(self)


      Build a path with '~' and '~user' patterns expanded


   .. method:: exists(self)


      Check whether I exist


   .. method:: isBlockDevice(self)


      Check whether I am a block device


   .. method:: isCharacterDevice(self)


      Check whether I am a character device


   .. method:: isDirectory(self)


      Check whether I am a directory


   .. method:: isFile(self)


      Check whether I am a regular file


   .. method:: isNamedPipe(self)


      Check whether I am a socket


   .. method:: isSocket(self)


      Check whether I am a socket


   .. method:: isSymlink(self)


      Check whether I am a symbolic link


   .. method:: mask(self, mask)


      Get my stat record and filter me through {mask}


   .. method:: mkdir(self, parents=False, exist_ok=False, **kwds)


      Create a directory at my location.

      If {parents} is {True}, create all necessary intermediate levels; if {exist_ok} is
      {True}, do not raise an exception if the directory exists already


   .. method:: touch(self, mode=1638, exist_ok=True)
      :abstractmethod:


      Create a file at his path


   .. method:: coerce(cls, *args)
      :classmethod:


      Build a path out of the given arguments


   .. method:: __str__(self)


      Assemble my parts into a string


   .. method:: __bool__(self)


      Test for non null values


   .. method:: __truediv__(self, other)


      Syntactic sugar for assembling paths


   .. method:: __rtruediv__(self, other)


      Syntactic sugar for assembling paths


   .. method:: _parse(cls, args, sep=_SEP, fragments=None)
      :classmethod:


      Recognize each entry in {args} and distill its contribution to the path under construction


   .. method:: _resolve(self, base=None, resolved=None)


      Workhorse for path resolution



.. data:: root
   

   

