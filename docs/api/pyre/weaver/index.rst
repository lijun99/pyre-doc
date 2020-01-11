:mod:`pyre.weaver`
==================

.. py:module:: pyre.weaver

.. autoapi-nested-parse::

   This package contains the machinery necessary to generate content in a variety of output formats.

   The primary target is human readable formats, such source code for programming languages.



Submodules
----------
.. toctree::
   :titlesonly:
   :maxdepth: 1

   Banner/index.rst
   BlockComments/index.rst
   BlockMill/index.rst
   C/index.rst
   CSh/index.rst
   Cfg/index.rst
   Cxx/index.rst
   Django/index.rst
   Expression/index.rst
   F77/index.rst
   F90/index.rst
   HTML/index.rst
   HTTP/index.rst
   Host/index.rst
   Indenter/index.rst
   Installation/index.rst
   Language/index.rst
   LineComments/index.rst
   LineMill/index.rst
   Make/index.rst
   Mill/index.rst
   MixedComments/index.rst
   PFG/index.rst
   Perl/index.rst
   Plexus/index.rst
   Project/index.rst
   ProjectTemplate/index.rst
   Python/index.rst
   SQL/index.rst
   SVG/index.rst
   Sh/index.rst
   Smith/index.rst
   Stationery/index.rst
   TeX/index.rst
   Weaver/index.rst
   XML/index.rst


Package Contents
----------------

.. py:class:: foundry(factory, implements=None, tip='', **kwds)

   A decorator for callables that return component classes

   .. attribute:: pyre_tip
      :annotation: = 

      

   .. attribute:: pyre_factory
      

      

   .. attribute:: pyre_implements
      

      

   .. method:: __call__(self, *args, **kwds)



   .. method:: sequify(self, items)
      :classmethod:


      Normalize {items} into a tuple



.. py:class:: weaver

   Bases: :class:`pyre.component`

   The base component for content generation

   .. attribute:: language
      

      

   .. attribute:: doc
      :annotation: = the desired output language

      

   .. method:: weave(self, **kwds)


      Assemble the {document}



.. py:class:: language

   Bases: :class:`pyre.protocol`

   The protocol specification for output languages

   .. attribute:: languages
      

      

   .. method:: pyre_convert(cls, value, **kwds)
      :classmethod:



   .. method:: render(self)


      Render the document


   .. method:: header(self)


      Render the header of the document


   .. method:: body(self)


      Render the body of the document


   .. method:: footer(self)


      Render the footer of the document



.. function:: mill()

   The base mill component


.. function:: line()

   The base mill component


.. function:: block()

   The base mill component


.. function:: c()

   The C weaver


.. function:: csh()

   The csh weaver


.. function:: cfg()

   The cfg weaver


.. function:: cxx()

   The C++ weaver


.. function:: f77()

   The FORTRAN weaver


.. function:: f90()

   The F90 weaver


.. function:: html()

   The HTML weaver


.. function:: http()

   The HTTP weaver


.. function:: make()

   The make weaver


.. function:: pfg()

   The pfg weaver


.. function:: perl()

   The perl weaver


.. function:: python()

   The python weaver


.. function:: sql()

   The SQL weaver


.. function:: svg()

   The SVG weaver


.. function:: sh()

   The sh weaver


.. function:: tex()

   The TeX weaver


.. function:: xml()

   The XML weaver


.. function:: smith(**kwds)

   The templater facility


.. py:class:: project

   Bases: :class:`pyre.protocol`

   Encapsulation of the project information

   .. attribute:: name
      

      

   .. attribute:: doc
      :annotation: = the name of the project

      

   .. attribute:: authors
      

      

   .. attribute:: doc
      :annotation: = the list of project authors

      

   .. attribute:: affiliations
      

      

   .. attribute:: doc
      :annotation: = the author affiliations

      

   .. attribute:: span
      

      

   .. attribute:: doc
      :annotation: = the project duration for the copyright message

      

   .. attribute:: live
      

      

   .. attribute:: doc
      :annotation: = information about the remote host

      

   .. method:: blacklisted(self, filename)


      Check whether {filename} is on the list of files to not expand


   .. method:: pyre_default(cls, **kwds)
      :classmethod:


      Build the preferred host implementation



.. function:: django()

   The django project type


.. function:: plexus()

   The plexus project type


