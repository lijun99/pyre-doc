:mod:`pyre.calc`
================

.. py:module:: pyre.calc

.. autoapi-nested-parse::

   This package provides the implementation of a simple evaluation network.

   There are three fundamental abstractions: variables, operators, and literals. Variables hold
   the values computed by the evaluation network, operators compute their values by acting on the
   values of other nodes, and literals encapsulate foreign objects, such as numeric constants.
   These abstractions provide the machinery for representing arbitrary expressions as graphs.

   The interesting aspect of this package is that nodal values get updated automatically when the
   values of any of the nodes in their domain change. Nodes keep track of the set of dependents
   that are interested in their values and post notifications when their values change.

   In addition, this package provides {SymbolTable}, a simple manager for evaluation nodes. Beyond
   node storage, {SymbolTable} enables the naming of nodes and can act as the name resolution
   context for {Expression} nodes, which evaluate strings with arbitrary python expressions that
   may involve the values of other nodes in the model. The other nodes provided here operate
   independently of {SymbolTable}. However, it is a good idea to build some kind of container to
   hold nodes while the evaluation graph is in use.

   Simple examples of the use of the ideas in this package are provided in the unit tests. For a
   somewhat more advanced example, take a look at {pyre.config.Configurator}, which is a
   {Hierarchical} model that builds an evaluation network out of the traits of pyre components, so
   that trait settings can refer to the values of other traits in the configuration files.



Submodules
----------
.. toctree::
   :titlesonly:
   :maxdepth: 1

   Average/index.rst
   Calculator/index.rst
   Composite/index.rst
   Const/index.rst
   Count/index.rst
   Datum/index.rst
   Dependency/index.rst
   Dependent/index.rst
   Evaluator/index.rst
   Expression/index.rst
   Filter/index.rst
   Hierarchical/index.rst
   Interpolation/index.rst
   Mapping/index.rst
   Maximum/index.rst
   Memo/index.rst
   Minimum/index.rst
   Node/index.rst
   NodeInfo/index.rst
   Observable/index.rst
   Observer/index.rst
   Postprocessor/index.rst
   Preprocessor/index.rst
   Probe/index.rst
   Product/index.rst
   Reactor/index.rst
   Reference/index.rst
   Sequence/index.rst
   Sum/index.rst
   SymbolTable/index.rst
   Unresolved/index.rst
   Value/index.rst
   exceptions/index.rst


Package Contents
----------------

.. py:class:: calculator

   Bases: :class:`pyre.algebraic.algebra`

   Metaclass that grants nodes value management capabilities

   .. method:: literalDerivation(cls, record)
      :classmethod:


      Contribute to the list of ancestors of the representation of literals


   .. method:: variableDerivation(cls, record)
      :classmethod:


      Contribute to the list of ancestors of the representation of literals


   .. method:: operatorDerivation(cls, record)
      :classmethod:


      Contribute to the list of ancestors of the representation of operators


   .. method:: sequenceDerivation(cls, record)
      :classmethod:


      Contribute to the list of ancestors of the representation of operators


   .. method:: mappingDerivation(cls, record)
      :classmethod:


      Contribute to the list of ancestors of the representation of operators


   .. method:: expressionDerivation(cls, record)
      :classmethod:


      Contribute to the list of ancestors of the representation of expressions


   .. method:: interpolationDerivation(cls, record)
      :classmethod:


      Contribute to the list of ancestors of the representation of interpolations


   .. method:: referenceDerivation(cls, record)
      :classmethod:


      Contribute to the list of ancestors of the representation of references


   .. method:: unresolvedDerivation(cls, record)
      :classmethod:


      Contribute to the list of ancestors of the representation of unresolved nodes


   .. method:: managedDependencyDerivation(cls)
      :classmethod:


      Build the canonical derivation of node that other nodes can depend on


   .. method:: managedDependentDerivation(cls)
      :classmethod:


      Place {dependent} in the right spot in the inheritance graph of {record}


   .. method:: managedCompositeDerivation(cls, composite, record)
      :classmethod:


      Place the class {composite} in the right spot in the {record} inheritance graph



.. function:: model(**kwds)

   Build a node container that specializes in names that have encoded hierarchical levels,
   such as file paths or namespaces


.. function:: var(value=None, **kwds)

   Build a variable, i.e. a node that can hold an arbitrary value


.. function:: expression(*, formula, model)

   Build a new node that evaluates a {formula} that involves the names of other nodes as
   resolved in the symbol table {model}.


.. function:: sequence(*operands)

   Build a node that holds a sequence of other nodes


.. function:: mapping(**operands)

   Build a node that holds a sequence of other nodes


.. function:: average(*operands)

   Compute the average of a collection of nodes


.. function:: count(*operands)

   Compute the length of a collection of nodes


.. function:: max(*operands)

   Compute the minimum of a collection of nodes


.. function:: min(*operands)

   Compute the minimum of a collection of nodes


.. function:: product(*operands)

   Compute the sum of a collection of nodes


.. function:: sum(*operands)

   Compute the sum of a collection of nodes


.. function:: debug()

   Support for debugging the calc package


