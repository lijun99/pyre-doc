:mod:`pyre.schemata.INet`
=========================

.. py:module:: pyre.schemata.INet


Module Contents
---------------

.. py:class:: Address

   Base class for addresses

   This class is useful when attempting to detect whether a value has already been converted
   to an internet address.

   .. method:: value(self)
      :property:




.. py:class:: IPv4(host='', port=None, **kwds)

   Bases: :class:`pyre.schemata.INet.Address`

   Encapsulation of an ipv4 socket address

   .. attribute:: family
      

      

   .. attribute:: host
      :annotation: = 

      

   .. attribute:: port
      :annotation: = 0

      

   .. method:: value(self)
      :property:


      Build the tuple required by {socket.connect}


   .. method:: __str__(self)




.. py:class:: Unix(path, **kwds)

   Bases: :class:`pyre.schemata.INet.Address`

   Unix domain sockets

   .. attribute:: family
      

      

   .. attribute:: path
      

      

   .. method:: value(self)
      :property:


      Build the value expected by {socket.connect}


   .. method:: __str__(self)




.. py:class:: INet(default=any, **kwds)

   Bases: :class:`pyre.schemata.Schema.Schema`

   A type declarator for internet addresses

   .. attribute:: address
      

      

   .. attribute:: any
      

      

   .. attribute:: typename
      :annotation: = inet

      

   .. attribute:: complaint
      :annotation: = could not coerce {0.value!r} into an internet address

      

   .. attribute:: regex
      

      

   .. method:: coerce(self, value, **kwds)


      Attempt to convert {value} into a internet address


   .. method:: recognize(self, family, address)


      Return an appropriate address type based on the socket family


   .. method:: parse(self, value)


      Convert {value}, expected to be a string, into an inet address


   .. method:: json(self, value)


      Generate a JSON representation of {value}



