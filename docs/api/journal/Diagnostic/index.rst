:mod:`journal.Diagnostic`
=========================

.. py:module:: journal.Diagnostic


Module Contents
---------------

.. py:class:: Diagnostic(name, **kwds)

   Encapsulation of the message recording behavior of channels

   .. attribute:: meta
      

      

   .. attribute:: text
      

      

   .. attribute:: locator
      

      

   .. attribute:: stackdepth
      

      

   .. method:: line(self, message='')


      Add {message} to the diagnostic text


   .. method:: log(self, message=None, stackdepth=0)


      Add the optional {message} to my text and make a journal entry



