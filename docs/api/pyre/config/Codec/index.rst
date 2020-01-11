:mod:`pyre.config.Codec`
========================

.. py:module:: pyre.config.Codec


Module Contents
---------------

.. py:class:: Codec

   The base class for readers/writers of the pyre configuration files

   .. attribute:: encoding
      

      

   .. method:: encode(self, item, stream)
      :classmethod:
      :abstractmethod:


      Build a representation of {item} in the current encoding and inject it into {stream}


   .. method:: decode(self, client, scheme, source, locator=None)
      :classmethod:
      :abstractmethod:


      Ingest {source} and return the decoded contents



