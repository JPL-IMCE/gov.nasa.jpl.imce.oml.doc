{% include "./external-links.md" %}
# OML Glossary of 35 Abstract Definitions

## OML Axiom

An OML Axiom maps to a pattern of [OWL2 Axioms].

{APIs: **Normalized**, **Functional**, **EMF/CDO**}

Abstract definition with 1 generalization:
 - OML TerminologyBoxStatement

and with 2 specializations:
 - OML ScalarOneOfLiteralAxiom
 - OML TermAxiom

## OML ConceptTreeDisjunction

An OML ConceptTreeDisjunction represents the root & non-leaf nodes of a concept taxonomy:
- Root node is a RootConceptTaxonomyAxiom.
- Non-leaf nodes are AnonymousConceptTaxonomyAxioms.

{APIs: **Normalized**, **Functional**, **EMF/CDO**}

Abstract with 2 specializations:
 - OML AnonymousConceptTaxonomyAxiom
 - OML RootConceptTaxonomyAxiom

## OML ConceptualEntity

An OML ConceptualEntity is an OML Entity
that can be either abstract or concrete.
An abstract OML ConceptualEntity cannot have any instance
in a final OML DescriptionBox.
A concrete OML ConceptualEntity can be partially instantiated
as an OML ConceptualEntitySingletonInstance in any OML DescriptionBox.
If is partially instantiated if some essential OML EntityRelationship
or OML DataRelationshipFromEntity with `isIdentityCriteria=true` lacks
an OML TerminologyInstanceAssertion specifying its reference or value respectively.

{APIs: **Normalized**, **Functional**, **EMF/CDO**}

Abstract with 2 specializations:
 - OML Concept
 - OML ReifiedRelationship

## OML ConceptualEntitySingletonInstance

An OML ConceptualEntitySingletonInstance defines an instance of an OML ConceptualEntity.
An OML ConceptualEntitySingletonInstance maps to an [OWL2 NamedIndividual].
The semantics depends on the kind of OML ConceptualEntity classifier:
- If the OML ConceptualEntity is the domain for at least at least
  one OML DataRelationshipFromEntity with `isIdentityCriteria=true`,
  then the [OWL2-DL] mapping includes an [OWL2 Key Axiom]
  forcing that all distinctly named OML ConceptualEntitySingletonInstance
  must have different values for each OML DataRelationshipFromEntity with `isIdentityCriteria=true`.
- otherwise, distinctly named OML ConceptualEntitySingletonInstance
  represent semantically different instances.

{APIs: **Normalized**, **Functional**, **EMF/CDO**}

Abstract definition with 1 generalization:
 - OML SingletonInstance

and with 2 specializations:
 - OML ConceptInstance
 - OML ReifiedRelationshipInstance

## OML Context

An OML Context maps to an [OWL2-DL Ontology];
it is a kind of OML Resource that is a logical container of OML TerminologyThings
and a non-logical container of OML Annotations.

{APIs: **Normalized**, **Functional**, **EMF/CDO**}

Abstract definition with 2 generalizations:
 - OML Resource
 - OML TerminologyThing

and with 2 specializations:
 - OML DescriptionBox
 - OML TerminologyBox

## OML DataRange

An OWL DataRange corresponds to an OWL2 DataRange with arity=1.

{APIs: **Normalized**, **Functional**, **EMF/CDO**}

Abstract definition with 1 generalization:
 - OML Datatype

and with 2 specializations:
 - OML RestrictedDataRange
 - OML Scalar

## OML DataRelationship

An OML DataRelationship is an OML DirectedBinaryRelationshipKind
where the domain or the range is some kind of OML Datatype.

{APIs: **Normalized**, **Functional**, **EMF/CDO**}

Abstract definition with 2 generalizations:
 - OML DirectedBinaryRelationshipKind
 - OML Term

and with 4 specializations:
 - OML EntityScalarDataProperty
 - OML EntityStructuredDataProperty
 - OML ScalarDataProperty
 - OML StructuredDataProperty

## OML DataRelationshipDomain

An OML DataRelationshipDomain is an abstraction
for the domain of an OML DataRelationship

{APIs: **Normalized**, **Functional**, **EMF/CDO**}

Abstract with 2 specializations:
 - OML DataRelationshipFromEntity
 - OML DataRelationshipFromStructure

## OML DataRelationshipFromEntity

An OML DataRelationshipFromEntity is an OML DataRelationship
whose domain is an OML Entity.

{APIs: **Normalized**, **Functional**, **EMF/CDO**}

Abstract definition with 1 generalization:
 - OML DataRelationshipDomain

and with 2 specializations:
 - OML EntityScalarDataProperty
 - OML EntityStructuredDataProperty

## OML DataRelationshipFromStructure

An OML DataRelationshipFromStructure is an OML DataRelationship
whose domain is an OML Structure.

{APIs: **Normalized**, **Functional**, **EMF/CDO**}

Abstract definition with 1 generalization:
 - OML DataRelationshipDomain

and with 2 specializations:
 - OML ScalarDataProperty
 - OML StructuredDataProperty

## OML DataRelationshipRange

An OML DataRelationshipRange is an abstraction
for the range of an OML DataRelationship

{APIs: **Normalized**, **Functional**, **EMF/CDO**}

Abstract with 2 specializations:
 - OML DataRelationshipToScalar
 - OML DataRelationshipToStructure

## OML DataRelationshipToScalar

An OML DataRelationshipToScalar is an OML DataRelationship
whose range is an OML DataRange.

{APIs: **Normalized**, **Functional**, **EMF/CDO**}

Abstract definition with 1 generalization:
 - OML DataRelationshipRange

and with 2 specializations:
 - OML EntityScalarDataProperty
 - OML ScalarDataProperty

## OML DataRelationshipToStructure

An OML DataRelationshipToStructure is an OML DataRelationship
whose range is an OML Structure.

{APIs: **Normalized**, **Functional**, **EMF/CDO**}

Abstract definition with 1 generalization:
 - OML DataRelationshipRange

and with 2 specializations:
 - OML EntityStructuredDataProperty
 - OML StructuredDataProperty

## OML Datatype

An OML Datatype is a common abstraction for what should be, in principle,
[OWL2 DataRange] of arity 1 (atomic) or > 1 (tuple structure).
In practice, an OML DataType maps to the [OWL2-DL] subset; which means
that an atomic OML Datatype maps to an [OWL2 Datatype] whereas
a structured OML Datatype maps to an [OWL2 Class].

{APIs: **Normalized**, **Functional**, **EMF/CDO**}

Abstract definition with 1 generalization:
 - OML Term

and with 2 specializations:
 - OML DataRange
 - OML Structure

## OML DirectedBinaryRelationshipKind

An OML DirectedBinaryRelationshipKind is an abstraction
for the category of OML Terms
that are relationships with arity 2

{APIs: **Normalized**, **Functional**, **EMF/CDO**}

Abstract with 4 specializations:
 - OML DataRelationship
 - OML DescriptionBoxExtendsClosedWorldDefinitions
 - OML DescriptionBoxRefinement
 - OML EntityRelationship

## OML DisjointUnionOfConceptsAxiom

An OML DisjointUnionOfConceptsAxioms represents non-leaf & leaf nodes of a concept taxonomy:
- Non-leaf nodes are AnonymousConceptTaxonomyAxioms.
- Leaf nodes are SpecificDisjointConceptAxioms.

{APIs: **Normalized**, **Functional**, **EMF/CDO**}

Abstract definition with 1 generalization:
 - OML TerminologyBundleStatement

and with 2 specializations:
 - OML AnonymousConceptTaxonomyAxiom
 - OML SpecificDisjointConceptAxiom

## OML Entity

An OML Entity is an abstraction for an OML Term
that is either an OML UnaryTermKind or
an OML DirectedBinaryRelationshipKind whose subject
and range are both a kind of OML Entity.

{APIs: **Normalized**, **Functional**, **EMF/CDO**}

Abstract definition with 1 generalization:
 - OML Term

and with 3 specializations:
 - OML Aspect
 - OML Concept
 - OML ReifiedRelationship

## OML EntityRelationship

An OML EntityRelationship is a kind of OML Term that
is an OML DirectedBinaryRelationshipKind between a
domain OML Entity and a range OML Entity.

{APIs: **Normalized**, **Functional**, **EMF/CDO**}

Abstract definition with 2 generalizations:
 - OML DirectedBinaryRelationshipKind
 - OML Term

and with 2 specializations:
 - OML ReifiedRelationship
 - OML UnreifiedRelationship

## OML EntityRestrictionAxiom

An OML EntityRestrictionAxiom maps to an [OWL2 Object Property Restiction]
for an OML EntityRelationship.

{APIs: **Normalized**, **Functional**, **EMF/CDO**}

Abstract definition with 1 generalization:
 - OML TermAxiom

and with 2 specializations:
 - OML EntityExistentialRestrictionAxiom
 - OML EntityUniversalRestrictionAxiom

## OML EntityScalarDataPropertyRestrictionAxiom

An OML EntityScalarDataPropertyRestrictionAxiom maps to
some kind of OWL2 Data Property Restriction.

{APIs: **Normalized**, **Functional**, **EMF/CDO**}

Abstract definition with 1 generalization:
 - OML TermAxiom

and with 3 specializations:
 - OML EntityScalarDataPropertyExistentialRestrictionAxiom
 - OML EntityScalarDataPropertyParticularRestrictionAxiom
 - OML EntityScalarDataPropertyUniversalRestrictionAxiom

## OML Resource

An OML Resource is an abstraction for
everything in a vocabulary that is identifiable
locally by name within the vocabulary and
globally by an IRI across multiple vocabularies.
For a particular OML Resource, the constraints
between its name and its IRI depend on what kind of OML Resource it is.

{APIs: **Normalized**, **Functional**, **EMF/CDO**}

Abstract with 3 specializations:
 - OML Context
 - OML SingletonInstance
 - OML Term

## OML RestrictedDataRange

An OML RestrictedDataRange corresponds to an OWL2 DataRange defined in terms of some kind of restriction of some other OML DataRange.
Instead of arbitrary OWL2 FacetRestrictionAxioms as constructors of OWL2 DataRanges,
the specializations of RestrictedDataRange correspond to the allowed restrictions in OWL2-DL datatype maps.
Node that the vocabulary of XSD fundamental facets is not included in OWL2-DL, consequently,
there is no support in OML for specifying datatype restrictions involving XSD fundamental facets as well.
@see https://www.w3.org/TR/owl2-syntax/#Data_Ranges
@see https://www.w3.org/TR/owl2-syntax/#Datatype_Maps

{APIs: **Normalized**, **Functional**, **EMF/CDO**}

Abstract definition with 1 generalization:
 - OML DataRange

and with 8 specializations:
 - OML BinaryScalarRestriction
 - OML IRIScalarRestriction
 - OML NumericScalarRestriction
 - OML PlainLiteralScalarRestriction
 - OML ScalarOneOfRestriction
 - OML StringScalarRestriction
 - OML SynonymScalarRestriction
 - OML TimeScalarRestriction

## OML SingletonInstance

An OML SingletonInstance defines an instance of either an OML ConceptualEntity or of an OML Structure.

{APIs: **Normalized**, **Functional**, **EMF/CDO**}

Abstract definition with 2 generalizations:
 - OML Resource
 - OML TerminologyInstanceAssertion

and with 2 specializations:
 - OML ConceptualEntitySingletonInstance
 - OML DataStructureTuple

## OML SpecializationAxiom

An OML SpecializationAxiom is a logical axiom
about a taxonomic relationship between a specific and a general OML Entity.

{APIs: **Normalized**, **Functional**, **EMF/CDO**}

Abstract definition with 1 generalization:
 - OML TermAxiom

and with 3 specializations:
 - OML AspectSpecializationAxiom
 - OML ConceptSpecializationAxiom
 - OML ReifiedRelationshipSpecializationAxiom

## OML Term

An OML Term map to the declaration of an [OWL2-DL Entity] of some kind.

{APIs: **Normalized**, **Functional**, **EMF/CDO**}

Abstract definition with 2 generalizations:
 - OML Resource
 - OML TerminologyBoxStatement

and with 4 specializations:
 - OML DataRelationship
 - OML Datatype
 - OML Entity
 - OML EntityRelationship

## OML TermAxiom

An OML TermAxiom is a logical axiom about an OML Term.

{APIs: **Normalized**, **Functional**, **EMF/CDO**}

Abstract definition with 1 generalization:
 - OML Axiom

and with 3 specializations:
 - OML EntityRestrictionAxiom
 - OML EntityScalarDataPropertyRestrictionAxiom
 - OML SpecializationAxiom

## OML TerminologyAxiom

An OML TerminologyAxiom is asserted in a TerminologyBox of some kind.

{APIs: **Normalized**, **Functional**, **EMF/CDO**}

Abstract definition with 1 generalization:
 - OML TerminologyThing

and with 2 specializations:
 - OML TerminologyBoxAxiom
 - OML TerminologyBundleAxiom

## OML TerminologyBox

An OML TerminologyBox is an OML Context for defining a domain-specific vocabulary
as a logical set of OML TerminologyBoxStatements,
possibly by reuse of other vocabularies via OML TerminologyBoxAxioms.
The semantics of an OML TerminologyBox domain-specific vocabulary is defined
by the mapping to [OWL2-DL] of the other vocabularies it reuses, if any, and
that of its OML TerminologyBoxAxioms and OML TerminologyBoxStatements
according to its OML TerminologyGraphKind.

{APIs: **Normalized**, **Functional**, **EMF/CDO**}

Abstract definition with 1 generalization:
 - OML Context

and with 2 specializations:
 - OML Bundle
 - OML TerminologyGraph

## OML TerminologyBoxAxiom

An OML TerminologyBoxAxiom is a TerminologyAxiom that asserts a logical statement about a Term.

{APIs: **Normalized**, **Functional**, **EMF/CDO**}

Abstract definition with 1 generalization:
 - OML TerminologyAxiom

and with 3 specializations:
 - OML ConceptDesignationTerminologyAxiom
 - OML TerminologyExtensionAxiom
 - OML TerminologyNestingAxiom

## OML TerminologyBoxStatement

An OML TerminologyBoxStatement is a logical axiom about an OML TerminologyThing
asserted in the context of an OML TerminologyBox.

{APIs: **Normalized**, **Functional**, **EMF/CDO**}

Abstract definition with 1 generalization:
 - OML TerminologyThing

and with 2 specializations:
 - OML Axiom
 - OML Term

## OML TerminologyBundleAxiom

An OML TerminologyBundleAxiom is a TerminologyAxiom that asserts a logical statement in the context of a Bundle.

{APIs: **Normalized**, **Functional**, **EMF/CDO**}

Abstract definition with 1 generalization:
 - OML TerminologyAxiom

and with 1 specialization:
 - OML BundledTerminologyAxiom

## OML TerminologyBundleStatement

An OML TerminologyBundleStatement is a logical axiom about an OML TerminologyThing
asserted in the context of an OML Bundle.

{APIs: **Normalized**, **Functional**, **EMF/CDO**}

Abstract definition with 1 generalization:
 - OML TerminologyThing

and with 2 specializations:
 - OML DisjointUnionOfConceptsAxiom
 - OML RootConceptTaxonomyAxiom

## OML TerminologyInstanceAssertion

An OML TerminologyInstanceAssertion is a logical OML TerminologyThing defined in an OML TerminologyDescription.

{APIs: **Normalized**, **Functional**, **EMF/CDO**}

Abstract definition with 1 generalization:
 - OML TerminologyThing

and with 6 specializations:
 - OML ReifiedRelationshipInstanceDomain
 - OML ReifiedRelationshipInstanceRange
 - OML ScalarDataPropertyValue
 - OML SingletonInstance
 - OML StructuredDataPropertyValue
 - OML UnreifiedRelationshipInstanceTuple

## OML TerminologyThing

An OML TerminologyThing is a logical abstraction for everything
in a vocabulary that is globally identified by a UUID.

{APIs: **Normalized**, **Functional**, **EMF/CDO**}

Abstract with 7 specializations:
 - OML Context
 - OML DescriptionBoxExtendsClosedWorldDefinitions
 - OML DescriptionBoxRefinement
 - OML TerminologyAxiom
 - OML TerminologyBoxStatement
 - OML TerminologyBundleStatement
 - OML TerminologyInstanceAssertion

## OML UnaryTermKind

An OML UnaryTermKind is an abstraction for the category of OML Terms
that are relationships with arity 1

{APIs: **Normalized**, **Functional**, **EMF/CDO**}

Abstract with 4 specializations:
 - OML Aspect
 - OML Concept
 - OML Scalar
 - OML Structure
