:mod:`pyre.xml.ElementDescriptor`
=================================

.. py:module:: pyre.xml.ElementDescriptor


Module Contents
---------------

.. py:class:: ElementDescriptor(*, tag, handler, root=False)

   Bases: :class:`pyre.xml.Descriptor.Descriptor`

   Descriptor class that gathers all the metadata about a document tag that was provided by
   the user during the DTD declaration. It is used by DTD derived classes to decorate the
   Document instance and the tag handlers with the information needed by the Reader so it can
   process XML documents

   .. attribute:: handler
      

      

   .. attribute:: attributes
      :annotation: = []

      


