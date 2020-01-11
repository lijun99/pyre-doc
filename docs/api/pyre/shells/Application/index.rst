:mod:`pyre.shells.Application`
==============================

.. py:module:: pyre.shells.Application


Module Contents
---------------

.. py:class:: Application(name=None, **kwds)

   Bases: :class:`pyre.component`

   Abstract base class for top-level application components

   {Application} streamlines the interaction with the pyre framework. It is responsible for
   staging an application process, i.e. establishing the process namespace and virtual
   filesystem, configuring the help system, and supplying the main behavior.

   .. attribute:: USER
      :annotation: = user

      

   .. attribute:: SYSTEM
      :annotation: = system

      

   .. attribute:: DEFAULTS
      :annotation: = defaults

      

   .. attribute:: pyre_namespace
      

      

   .. attribute:: shell
      

      

   .. attribute:: doc
      :annotation: = my hosting strategy

      

   .. attribute:: DEBUG
      

      

   .. attribute:: doc
      :annotation: = debugging mode

      

   .. attribute:: pyre_home
      

      

   .. attribute:: pyre_prefix
      

      

   .. attribute:: pyre_defaults
      

      

   .. attribute:: pfs
      

      

   .. attribute:: layout
      

      

   .. attribute:: pyre_renderer
      

      

   .. attribute:: info
      

      

   .. attribute:: warning
      

      

   .. attribute:: error
      

      

   .. attribute:: debug
      

      

   .. attribute:: firewall
      

      

   .. method:: executive(self)
      :property:


      Provide access to the pyre executive


   .. method:: vfs(self)
      :property:


      Easy access to the executive file server


   .. method:: nameserver(self)
      :property:


      Easy access to the executive name server


   .. method:: argv(self)
      :property:


      Return an iterable over the command line arguments that were not configuration options


   .. method:: searchpath(self)
      :property:


      Build a list of unique package names from my ancestry in mro order


   .. method:: main(self, *args, **kwds)


      The main entry point of an application component


   .. method:: launched(self, *args, **kwds)


      Notification issued by some shells that application launching is complete


   .. method:: help(self, **kwds)


      Hook for the application help system


   .. method:: run(self, *args, **kwds)


      Ask my shell to launch me


   .. method:: pyre_loadLayout(self)


      Create my application layout object, typically a subclass of {pyre.shells.Layout}


   .. method:: pyre_explore(self)


      Look around my runtime environment and the filesystem for my special folders


   .. method:: pyre_mountPrivateFilespace(self)


      Build the private filesystem


   .. method:: pyre_mountApplicationFolders(self, pfs, prefix)


      Explore the application installation folders and construct my private filespace


   .. method:: pyre_mountPrivateFolder(self, pfs, prefix, folder)


      Look in {prefix} for {folder}, create it if necessary, and mount it within {pfs}, my
      private filespace


   .. method:: pyre_resolveDependencies(self)


      Go through my list of required package categories and resolve them

      The result is a map from package categories to package instances that satisfy each
      requirement. This map includes dependencies induced while trying to satisfy my
      requirements


   .. method:: pyre_shutdown(self, **kwds)


      Release all resources and prepare to exit


   .. method:: pyre_interrupted(self, **kwds)


      The user issued a keyboard interrupt


   .. method:: pyre_interactiveSessionContext(self, context)


      Prepare the interactive context by granting access to application parts


   .. method:: pyre_interactiveBanner(self)


      Print an identifying message for the interactive session


   .. method:: pyre_help(self, indent=' ' * 4, **kwds)


      Hook for the application help system


   .. method:: pyre_banner(self)


      Print an identifying message for the help system


   .. method:: pyre_respond(self, server, request)


      Fulfill a request from an HTTP {server}



