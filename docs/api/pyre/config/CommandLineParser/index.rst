:mod:`pyre.config.CommandLineParser`
====================================

.. py:module:: pyre.config.CommandLineParser


Module Contents
---------------

.. py:class:: CommandLineParser(handlers=None, **kwds)

   Support for parsing the application command line

   The general form of a command line configuration event is
       --key=value
   which creates a configuration event that will bind {key} to {value}.

   This implementation supports the following constructs:
       --key
           set key to None
       --key=value
       --key.subkey=value
           key may have an arbitrary number of period delimited levels
       --(key1,key2)=value
           equivalent to --key1=value and --key2=value; an arbitrary number of comma separated
           key names are allowed
       --key.(key1,key2)=value
       --key.(key1,key2).key3=value
           as above; this form is supported at any level of the hierarchy

   By default, instances of the command line parser use the following literals
       '-': introduces a configuration command
       '=': indicates an assignment
       '.': the separator for multi-level keys
       '(' and ')': the start and end of a key group
       ',': the separator for keys in a group

   If you want to change any of this, you can instantiate a command line parser, modify any of
   its public data, and invoke "buildScanners" to recompute the associated regular expression
   engines

   .. attribute:: prefix
      :annotation: = -

      

   .. attribute:: assignment
      :annotation: = =

      

   .. attribute:: fieldSeparator
      :annotation: = .

      

   .. attribute:: groupStart
      :annotation: = (

      

   .. attribute:: groupSeparator
      :annotation: = ,

      

   .. attribute:: groupEnd
      :annotation: = )

      

   .. attribute:: handlers
      

      

   .. attribute:: assignmentScanner
      

      

   .. attribute:: locator
      

      

   .. method:: parse(self, argv)


      Harvest the configuration events in {argv} and store them in a {configuration}

      parameters:
          {argv}: a container of strings of the form "--key=value"
          {locator}: an optional locator; not used by this decoder


   .. method:: buildScanners(self)


      Build the command line recognizers that are used to detect the supported command line
      argument syntactical forms


   .. method:: _processAssignments(self, configuration, key, value, locator)


      Handler for command line arguments that were interpreted as assignments

      Look for the supported shorthands and unfold them into canonical forms.


   .. method:: _processArguments(self, configuration, index, *args)


      Interpret {args} as application commands and store them in {configuration}



