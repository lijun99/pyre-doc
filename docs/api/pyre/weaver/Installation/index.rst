:mod:`pyre.weaver.Installation`
===============================

.. py:module:: pyre.weaver.Installation


Module Contents
---------------

.. py:class:: Installation

   Bases: :class:`pyre.protocol`

   Encapsulation of the configuration and layout of the machine hosting the installation

   .. attribute:: name
      

      

   .. attribute:: doc
      :annotation: = the name of the machine that hosts the live application

      

   .. attribute:: virtual
      

      

   .. attribute:: doc
      :annotation: = the virtual name of the web server

      

   .. attribute:: home
      

      

   .. attribute:: doc
      :annotation: = the home directory of the remote user hosting the installation

      

   .. attribute:: root
      

      

   .. attribute:: doc
      :annotation: = the installation directory on the hosting machine

      

   .. attribute:: web
      

      

   .. attribute:: doc
      :annotation: = the location of web related directories at the hosting machine

      

   .. attribute:: admin
      

      

   .. attribute:: doc
      :annotation: = the username of the remote administrator

      

   .. method:: pyre_default(cls, **kwds)
      :classmethod:


      Build the preferred host implementation



