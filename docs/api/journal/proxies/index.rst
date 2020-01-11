:mod:`journal.proxies`
======================

.. py:module:: journal.proxies


Module Contents
---------------

.. function:: debugIndex()

   Build an object that is a wrapper around the debug channel index from the C++
   extension. i.e. {pyre::journal::debug_t::index_t}


.. function:: firewallIndex()

   Build an object that is a wrapper around the firewall channel index from the C++
   extension. i.e. {pyre::journal::firewall_t::index_t}


.. function:: infoIndex()

   Build an object that is a wrapper around the info channel index from the C++
   extension. i.e. {pyre::journal::info_t::index_t}


.. function:: warningIndex()

   Build an object that is a wrapper around the warning channel index from the C++
   extension. i.e. {pyre::journal::warning_t::index_t}


.. function:: errorIndex()

   Build an object that is a wrapper around the error channel index from the C++
   extension. i.e. {pyre::journal::error_t::index_t}


.. py:class:: Index(lookup, inventory)

   Wrapper around the C++ diagnostic indices from the journal extension module

   .. method:: __getitem__(self, name)


      Retrieve the state associated with the given {name}



.. py:class:: Enabled(capsule)

   Wrapper around {pyre::journal::Inventory<true>}

   .. attribute:: device
      

      

   .. method:: state(self)
      :property:




.. py:class:: Disabled(capsule)

   Wrapper around {pyre::journal::Inventory<false>}

   .. attribute:: device
      

      

   .. method:: state(self)
      :property:




