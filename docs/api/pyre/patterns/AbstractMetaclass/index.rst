:mod:`pyre.patterns.AbstractMetaclass`
======================================

.. py:module:: pyre.patterns.AbstractMetaclass


Module Contents
---------------

.. py:class:: AbstractMetaclass(name, bases, attributes, **kwds)

   Bases: :class:`type`

   The base metaclass from which all pyre metaclasses derive.

   The main raison d'être for this class is to lift the constraint that the signatures of the
   various metaclass hooks must absorb all arguments passed through {**kwds} before invoking
   their implementations in {type}.

   implementation details:
     __new__: swallow the **kwds that {type} does not recognize
     __init__: swallow the **kwds that {type} does not recognize


