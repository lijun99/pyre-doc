:mod:`journal.Error`
====================

.. py:module:: journal.Error


Module Contents
---------------

.. py:class:: Error

   Bases: :class:`journal.Diagnostic.Diagnostic`, :class:`journal.Channel.Channel`

   This class is the implementation of the error channel

   .. attribute:: severity
      :annotation: = error

      

   .. attribute:: _index
      

      

   .. attribute:: stackdepth
      

      

   .. method:: log(self, message=None, stackdepth=0)


      Make a journal entry and build an exception ready to be raised by the caller



