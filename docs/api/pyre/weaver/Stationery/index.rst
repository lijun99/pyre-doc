:mod:`pyre.weaver.Stationery`
=============================

.. py:module:: pyre.weaver.Stationery


Module Contents
---------------

.. py:class:: Stationery

   Bases: :class:`pyre.protocol`

   The protocol that layout strategies must implement

   .. attribute:: width
      

      

   .. attribute:: doc
      :annotation: = the preferred width of the generated text

      

   .. attribute:: authors
      

      

   .. attribute:: doc
      :annotation: = the name of the entities to blame for this content

      

   .. attribute:: affiliation
      

      

   .. attribute:: doc
      :annotation: = the author's institutional affiliation

      

   .. attribute:: copyright
      

      

   .. attribute:: doc
      :annotation: = the copyright notice

      

   .. attribute:: license
      

      

   .. attribute:: doc
      :annotation: = the license

      

   .. attribute:: footer
      

      

   .. attribute:: doc
      :annotation: = the marker to drop at the bottom of the document

      

   .. method:: pyre_default(cls, **kwds)
      :classmethod:


      Choose a layout as the default



