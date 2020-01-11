:mod:`pyre.shells`
==================

.. py:module:: pyre.shells

.. autoapi-nested-parse::

   This package provides support for composing pyre applications

   The pyre framework encourages factoring applications into two distinct parts: a subclass of the
   component {Application} that defines the runtime behavior of the application, and a hosting
   strategy that defines the runtime environment in which the application executes. The hosting
   strategy is a subclass of the component {Shell} and is responsible for creating the execution
   context for the application.

   The package provides a number of ready to use hosting strategies.

   {Script} expects an instance of an {Application} subclass, invokes its {main} method, and exits
   after handing the value returned to the operating system as the process exit code. It the pyre
   equivalent of the familiar launching of executables written in low level languages.

   {Daemon} is suitable for applications that run in the background, without access to a
   terminal. It performs the steps necessary to detach a process from its parent so that the
   parent may exit without causing the child to terminate as well.

   {Service} builds on {Daemon} to enable distributed applications by exposing the application
   component registry to the network.

   Other packages leverage these building blocks to provide support for other hosting
   strategies. For a sophisticated example, see the {mpi} package, which provides support for
   running concurrent applications using {MPI}.



Submodules
----------
.. toctree::
   :titlesonly:
   :maxdepth: 1

   ANSI/index.rst
   ASCII/index.rst
   Action/index.rst
   Application/index.rst
   CSI/index.rst
   Command/index.rst
   Daemon/index.rst
   Director/index.rst
   Executive/index.rst
   Fork/index.rst
   IPython/index.rst
   Interactive/index.rst
   Layout/index.rst
   Panel/index.rst
   Plain/index.rst
   Plexus/index.rst
   Renderer/index.rst
   Repertoir/index.rst
   Script/index.rst
   Shell/index.rst
   Terminal/index.rst
   User/index.rst
   Web/index.rst


Package Contents
----------------

.. py:class:: foundry(factory, implements=None, tip='', **kwds)

   A decorator for callables that return component classes

   .. attribute:: pyre_tip
      :annotation: = 

      

   .. attribute:: pyre_factory
      

      

   .. attribute:: pyre_implements
      

      

   .. method:: __call__(self, *args, **kwds)



   .. method:: sequify(self, items)
      :classmethod:


      Normalize {items} into a tuple



.. py:class:: action

   Bases: :class:`pyre.protocol`

   A protocol that facilitates application extensibility: components that implement {Action}
   can be invoked from the command line

   .. method:: main(self, *kwds)


      This is the implementation of the action


   .. method:: help(self, **kwds)


      Provide help with invoking this action


   .. method:: pyre_documentedActions(cls)
      :classmethod:


      Retrieve all visible implementations that are documented



.. function:: command()

   The command base component


.. function:: panel()

   The command panel base component


.. py:class:: shell

   Bases: :class:`pyre.protocol`

   The protocol implemented by the pyre application hosting strategies

   .. attribute:: home
      

      

   .. attribute:: doc
      :annotation: = the process home directory

      

   .. attribute:: hosts
      

      

   .. attribute:: doc
      :annotation: = the number of hosts in the parallel machine

      

   .. attribute:: tasks
      

      

   .. attribute:: doc
      :annotation: = the number of tasks per host

      

   .. attribute:: gpus
      

      

   .. attribute:: doc
      :annotation: = the number of GPU coprocessors per task

      

   .. attribute:: model
      

      

   .. attribute:: doc
      :annotation: = the programming model

      

   .. method:: pyre_default(cls, **kwds)
      :classmethod:


      The default shell implementation


   .. method:: launch(self, application, *args, **kwds)


      Launch the application



.. function:: script()

   The basic application shell


.. function:: interactive()

   An application shell based on {script} that enters interactive mode after the application
   is finished running


.. function:: ipython()

   An application shell based on {script} that enters interactive mode after the application
   is finished running


.. function:: fork()

   The fork shell: a shell that invokes the application main entry point in a child process


.. function:: daemon()

   The daemon shell: a shell that invokes the application main entry point as long lived
   independent process that has detached completely from its parent


.. function:: web()

   The web shell: an interactive shell that presents the user with an initial web page


.. py:class:: terminal

   Bases: :class:`pyre.protocol`

   An abstraction for the capabilities of user terminals

   .. attribute:: ansi
      

      

   .. method:: pyre_default(cls, **kwds)
      :classmethod:


      Sniff out the capabilities of the current terminal and choose the default implementation



.. function:: ansi()

   A terminal that supports color control using ANSI escpae sequences


.. function:: plain()

   A plain terminal with no special capabilities


.. py:class:: application(name=None, **kwds)

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



.. py:class:: plexus(**kwds)

   Bases: :class:`pyre.shells.Application.Application`

   Base class for applications that interpret their first non-configurational command line
   argument as an action that should be executed.

   As an example of such an app, consider {merlin}. Invoking

       merlin version

   causes the {merlin} plexus to locate an action named {version} and invoke it.

   Subclasses are expected to declare a class variable {pyre_action} that points to a subclass
   of the {Action} protocol defined in this package. This responsibility is left to subclasses
   so that there is no bias on the category names of the actions induced by a choice of family
   name by the framework. This way the language used to specify the actions and their behavior
   can remain natural to the context of the application.

   .. attribute:: pyre_repertoir
      

      

   .. method:: main(self, *args, **kwds)


      The plexus main entry point interprets the first non-configurational command line argument
      as the name of an action to perform


   .. method:: help(self, **kwds)


      Hook for the application help system


   .. method:: pyre_newRepertoir(self)


      Factory for the manager of actions


   .. method:: pyre_invoke(self, action, argv)


      Invoke the named {action} with {argv} as additional arguments


   .. method:: pyre_documentActions(self, indent=' ' * 4)


      Place information about the available actions in my {info} channel



.. py:class:: layout

   Bases: :class:`pyre.component`

   A collection of configuration options that define the deployment layout of a pyre application

   .. attribute:: project
      

      

   .. attribute:: doc
      :annotation: = the nickname of this application deployment

      

   .. attribute:: etc
      

      

   .. attribute:: doc
      :annotation: = the location of application auxiliary data

      

   .. attribute:: var
      

      

   .. attribute:: doc
      :annotation: = the location of files that support the application runtime environment

      


.. py:class:: user

   Bases: :class:`pyre.component`

   Encapsulation of user specific information

   .. attribute:: name
      

      

   .. attribute:: doc
      :annotation: = the full name of the user

      

   .. attribute:: email
      

      

   .. attribute:: doc
      :annotation: = the email address of the user

      

   .. attribute:: affiliation
      

      

   .. attribute:: doc
      :annotation: = the affiliation of the user

      

   .. attribute:: externals
      

      

   .. attribute:: doc
      :annotation: = the database of preferred instances for each external package category

      

   .. attribute:: uid
      

      

   .. attribute:: home
      

      

   .. attribute:: username
      

      


