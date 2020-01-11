:mod:`pyre.http.Response`
=========================

.. py:module:: pyre.http.Response


Module Contents
---------------

.. py:exception:: Response(server, version=version, encoding=encoding, **kwds)

   Bases: :class:`pyre.nexus.exceptions.NexusError`

   The base class for all http server responses.

   .. attribute:: code
      

      

   .. attribute:: status
      :annotation: = 

      

   .. attribute:: server
      

      

   .. attribute:: headers
      

      

   .. attribute:: encoding
      :annotation: = utf-8

      

   .. attribute:: version
      :annotation: = [1, 1]

      

   .. attribute:: months
      :annotation: = [None, 'Jan', 'Feb', 'Mar', 'Apr', 'May', 'Jun', 'Jul', 'Aug', 'Sep', 'Oct', 'Nov', 'Dec']

      

   .. attribute:: weekdays
      :annotation: = ['Mon', 'Tue', 'Wed', 'Thu', 'Fri', 'Sat', 'Sun']

      

   .. method:: timestamp(self, tick=None)


      Generate a conforming timestamp



