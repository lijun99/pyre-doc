:mod:`journal`
==============

.. py:module:: journal


Submodules
----------
.. toctree::
   :titlesonly:
   :maxdepth: 1

   ANSIRenderer/index.rst
   Channel/index.rst
   Console/index.rst
   Debug/index.rst
   Device/index.rst
   Diagnostic/index.rst
   Error/index.rst
   File/index.rst
   Firewall/index.rst
   Info/index.rst
   Journal/index.rst
   Renderer/index.rst
   TextRenderer/index.rst
   Warning/index.rst
   exceptions/index.rst
   protocols/index.rst
   proxies/index.rst
   schemes/index.rst


Package Contents
----------------

.. function:: copyright()

   Return the pyre journal copyright note


.. function:: license()

   Print the pyre journal license


.. function:: version()

   Return the pyre journal version


.. data:: _journal_version
   :annotation: = [1, 0, 0]

   

.. data:: _journal_copyright
   :annotation: = pyre journal: Copyright (c) 1998-2019 Michael A.G. Aïvázis

   

.. data:: _journal_license
   :annotation: = 
    pyre journal 1.0
    Copyright (c) 1998-2019 Michael A.G. Aïvázis
    All Rights Reserved


    Redistribution and use in source and binary forms, with or without
    modification, are permitted provided that the following conditions
    are met:

    * Redistributions of source code must retain the above copyright
      notice, this list of conditions and the following disclaimer.

    * Redistributions in binary form must reproduce the above copyright
      notice, this list of conditions and the following disclaimer in
      the documentation and/or other materials provided with the
      distribution.

    * Neither the name pyre nor the names of its contributors may be
      used to endorse or promote products derived from this software
      without specific prior written permission.

    THIS SOFTWARE IS PROVIDED BY THE COPYRIGHT HOLDERS AND CONTRIBUTORS
    "AS IS" AND ANY EXPRESS OR IMPLIED WARRANTIES, INCLUDING, BUT NOT
    LIMITED TO, THE IMPLIED WARRANTIES OF MERCHANTABILITY AND FITNESS
    FOR A PARTICULAR PURPOSE ARE DISCLAIMED. IN NO EVENT SHALL THE
    COPYRIGHT OWNER OR CONTRIBUTORS BE LIABLE FOR ANY DIRECT, INDIRECT,
    INCIDENTAL, SPECIAL, EXEMPLARY, OR CONSEQUENTIAL DAMAGES (INCLUDING,
    BUT NOT LIMITED TO, PROCUREMENT OF SUBSTITUTE GOODS OR SERVICES;
    LOSS OF USE, DATA, OR PROFITS; OR BUSINESS INTERRUPTION) HOWEVER
    CAUSED AND ON ANY THEORY OF LIABILITY, WHETHER IN CONTRACT, STRICT
    LIABILITY, OR TORT (INCLUDING NEGLIGENCE OR OTHERWISE) ARISING IN
    ANY WAY OUT OF THE USE OF THIS SOFTWARE, EVEN IF ADVISED OF THE
    POSSIBILITY OF SUCH DAMAGE.
    

   

.. function:: boot()

   Initialize the journal package.

   Attempt to locate the C++ extension and use it if available; fall back on the pure python
   implementation. Either way, return a marker that enables clients to check whether there is
   support for journal messages from C/C++/FORTRAN.


.. data:: package
   

   

.. py:class:: debug

   Bases: :class:`journal.Diagnostic.Diagnostic`, :class:`journal.Channel.Channel`

   This class is the implementation of the debug channel

   .. attribute:: severity
      :annotation: = debug

      

   .. attribute:: _index
      

      


.. py:class:: firewall

   Bases: :class:`journal.Diagnostic.Diagnostic`, :class:`journal.Channel.Channel`

   This class is the implementation of the firewall channel

   .. attribute:: fatal
      :annotation: = False

      

   .. attribute:: severity
      :annotation: = firewall

      

   .. attribute:: _index
      

      

   .. attribute:: stackdepth
      

      

   .. method:: log(self, message=None, stackdepth=0)


      Record my message to my device



.. py:class:: info

   Bases: :class:`journal.Diagnostic.Diagnostic`, :class:`journal.Channel.Channel`

   This class is the implementation of the info channel

   .. attribute:: severity
      :annotation: = info

      

   .. attribute:: _index
      

      


.. py:class:: warning

   Bases: :class:`journal.Diagnostic.Diagnostic`, :class:`journal.Channel.Channel`

   This class is the implementation of the warning channel

   .. attribute:: severity
      :annotation: = warning

      

   .. attribute:: _index
      

      


.. py:class:: error

   Bases: :class:`journal.Diagnostic.Diagnostic`, :class:`journal.Channel.Channel`

   This class is the implementation of the error channel

   .. attribute:: severity
      :annotation: = error

      

   .. attribute:: _index
      

      

   .. attribute:: stackdepth
      

      

   .. method:: log(self, message=None, stackdepth=0)


      Make a journal entry and build an exception ready to be raised by the caller



.. py:class:: console

   Bases: :class:`pyre.component`

   A device that sends journal messages to the standard output

   .. attribute:: renderer
      

      

   .. attribute:: doc
      :annotation: = the formatting strategy for journal entries

      

   .. method:: record(self, page, metadata)


      Record a journal entry



.. py:class:: file

   Bases: :class:`pyre.component`

   This is a sample documentation string for class Console

   .. attribute:: log
      

      

   .. attribute:: doc
      :annotation: = the file in which to save the journal entries

      

   .. attribute:: renderer
      

      

   .. attribute:: doc
      :annotation: = the formatting strategy for journal entries

      

   .. method:: record(self, page, metadata)


      Record a journal entry



.. py:exception:: FirewallError(firewall, **kwds)

   Bases: :class:`pyre.framework.exceptions.PyreError`

   Exception raised whenever a fatal firewall is encountered

   .. attribute:: description
      :annotation: = firewall breached; aborting...

      


.. data:: extension
   

   

