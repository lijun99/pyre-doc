:mod:`journal.exceptions`
=========================

.. py:module:: journal.exceptions


Module Contents
---------------

.. py:exception:: FirewallError(firewall, **kwds)

   Bases: :class:`pyre.framework.exceptions.PyreError`

   Exception raised whenever a fatal firewall is encountered

   .. attribute:: description
      :annotation: = firewall breached; aborting...

      


.. py:exception:: ApplicationError(error, **kwds)

   Bases: :class:`pyre.framework.exceptions.PyreError`

   Exception raised whenever an application error is encountered

   .. attribute:: description
      :annotation: = firewall breached; aborting...

      


