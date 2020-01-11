:mod:`pyre.externals.Installation`
==================================

.. py:module:: pyre.externals.Installation


Module Contents
---------------

.. py:class:: Installation

   Bases: :class:`pyre.component`

   Base class for all package installations

   .. attribute:: category
      :annotation: = unknown

      

   .. attribute:: version
      

      

   .. attribute:: doc
      :annotation: = the package version

      

   .. attribute:: prefix
      

      

   .. attribute:: doc
      :annotation: = the package installation directory

      

   .. attribute:: _misconfigured
      :annotation: = False

      

   .. method:: majorver(self)
      :property:


      Extract the portion of a version number that is used to label my parts


   .. method:: sigver(self)
      :property:


      Extract the portion of a version number that is used to label my parts


   .. method:: pyre_configured(self)


      Verify the package configuration


   .. method:: pyre_initialized(self)


      Attempt to repair broken configurations


   .. method:: verify(self, trait, patterns=(), folders=())


      Verify that {trait} properly configured by checking that every file name in {patterns}
      exists in one of the {folders}


   .. method:: commonpath(self, folders)


      Find the longest prefix common to the given {folders}


   .. method:: join(self, folders, prefix='')


      Render the sequence of {folders} as a flat string with each one prefixed by {prefix}



