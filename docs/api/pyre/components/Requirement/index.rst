:mod:`pyre.components.Requirement`
==================================

.. py:module:: pyre.components.Requirement


Module Contents
---------------

.. py:class:: Requirement

   Bases: :class:`pyre.patterns.AttributeClassifier.AttributeClassifier`

   Metaclass that enables the harvesting of trait declarations

   This class captures the class record processing that is common to both interfaces and
   components. Given a declaration record, {Requirement}

     * discovers the bases classes that are configurables
     * identifies the specially marked attributes
     * creates the namemap that handles trait name aliasing

   .. method:: pyre_getLocalTraits(self, attributes)


      Scan the dictionary {attributes} for trait descriptors


   .. method:: pyre_getInheritedTraits(self, shadowed)


      Look through the ancestors of {configurable} for traits whose name are not members of
      {shadowed}, the set of names that are inaccessible.


   .. method:: pyre_getPedigree(self)


      Visit my ancestors and locate the ones that are themselves configurables


   .. method:: pyre_getEigenPedigree(self)


      Build a sequence of my ancestors that are configurable and NOT related to each other
      through inheritance


   .. method:: pyre_isComponent(self, configurable)
      :classmethod:


      Check whether {configurable} is a component


   .. method:: pyre_isProtocol(self, configurable)
      :classmethod:


      Check whether {configurable} is a protocol



