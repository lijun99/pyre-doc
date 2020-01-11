:mod:`pyre.shells.Plexus`
=========================

.. py:module:: pyre.shells.Plexus


Module Contents
---------------

.. py:class:: Plexus(**kwds)

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



