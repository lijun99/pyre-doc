:mod:`pyre.weaver.Project`
==========================

.. py:module:: pyre.weaver.Project


Module Contents
---------------

.. py:class:: Project

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



