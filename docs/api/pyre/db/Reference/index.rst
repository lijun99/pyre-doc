:mod:`pyre.db.Reference`
========================

.. py:module:: pyre.db.Reference


Module Contents
---------------

.. py:class:: Reference(**kwds)

   Bases: :class:`pyre.db.Measure.Measure`

   Representation of foreign keys

   .. method:: decl(self)
      :property:


      SQL rendering of my type name


   .. method:: sql(self, value)


      SQL rendering of {value}


   .. method:: onDelete(self, action)


      Set the action to perform when the target record is deleted. See {pyre.db.actions} for
      details


   .. method:: onUpdate(self, action)


      Set the action to perform when the target record is updated. See {pyre.db.actions} for
      details



