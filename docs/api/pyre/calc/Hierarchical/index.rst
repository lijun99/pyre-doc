:mod:`pyre.calc.Hierarchical`
=============================

.. py:module:: pyre.calc.Hierarchical


Module Contents
---------------

.. py:class:: Hierarchical(separator=separator, **kwds)

   Bases: :class:`pyre.calc.SymbolTable.SymbolTable`

   Storage and naming services for algebraic nodes

   This class assumes that the node names form a hierarchy, very much like path
   names. Subclasses define what the level separator is; {Hierarchical} is shielded from this
   decision by expecting names to be iterables of strings specifying the name of each level.

   {Hierarchical} provides support for links, entries that are alternate names for other
   folders.

   .. attribute:: separator
      :annotation: = .

      

   .. attribute:: _hash
      

      

   .. attribute:: _info
      

      

   .. method:: children(self, key)


      Given the address {key} of a node, iterate over all the canonical nodes that are
      its logical children


   .. method:: find(self, pattern='', key=None)


      Generate a sequence of (name, node) pairs for all nodes in the model whose name
      matches the supplied {pattern}. Careful to properly escape periods and other characters
      that may occur in the name of the requested keys that are recognized by the {re}
      package. The order in which the nodes are returned is controlled by {key}.


   .. method:: alias(self, target, alias, base=None)


      Within the context of {base}, register the name {alias} as an alternate name for
      {target}. The net effect is to make {base.alias} point to {target}.

      parameters:
        {target}: the canonical name/key that owns the associated node
         {alias}: the alternate name, a string with no implied structure
          {base}: the context name/key within which the alias is established;
                  defaults to global scope

      If both {target} and {alias} exist, an exception is raised; if the caller ignores this
      exception, the net effect is to make the {target} value accessible under both names,
      and discard the value previously registered under {alias}.


   .. method:: hash(self, name, context=None)


      Split a multilevel {name} into its parts and return its hash


   .. method:: insert(self, key, value, name=None)


      Register the new {node} in the model under {name}


   .. method:: getInfo(self, key)


      Retrieve the metadata of the node registered under {key}


   .. method:: getNode(self, key)


      Retrieve the node registered under {key}


   .. method:: getName(self, key)


      Retrieve the name of the node registered under {key}


   .. method:: getSplitName(self, key)


      Retrieve the sequence of fragments in the name of the node registered under {key}


   .. method:: retrieve(self, name)


      Retrieve the node registered under {name}. If no such node exists, an error marker will
      be built, stored in the symbol table under {name}, and returned.


   .. method:: split(self, name)


      Take {name} apart using my separator


   .. method:: join(self, *levels)


      Form the canonical name of a key by joining {levels} using my separator


   .. method:: __contains__(self, name)


      Check whether {item} is present in the table


   .. method:: __setitem__(self, name, value)


      Convert {value} into a node and update the model


   .. method:: merge(self, source, canonical, destination, name)


      Merge the information associated with {source} into {destination} under {name}.

      Both {source} and {destination} are assumed to be valid hash keys, while {name} is a
      string with no key structure.


   .. method:: store(self, key, name, node, info)


      Associate {name}, {node} and {info} with {key}


   .. method:: replace(self, key, name, oldNode, oldInfo, newNode, newInfo)


      Choose which settings to retain


   .. method:: dump(self, pattern='')


      List my contents



