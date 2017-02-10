# Glossary

## OML Annotation

An OML Annotation maps to an [OWL2 Annotation] and is similarly
a non-logical statement in the context of an OML Terminology
associating some information as the value of an
OML AnnotationProperty for describing a subject (an OML TerminologyThing).

## OML AnnotationEntry

In the OML tabular interchange representation,
an OML AnnotationEntry (for a given OML AnnotationProperty) is a triple:
- the terminology in which the annotation appears
- the annotated terminology thing (subject)
- the value of the AnnotationProperty for that subject in that terminology

## OML AnnotationProperty

An OML AnnotationProperty maps to an [OWL2 AnnotationProperty]
and is similarly a non-logical property for associating some information
to any OML TerminologyThing in the context of an OML TerminologyBox.

## OML AnnotationPropertyTable

For the OML tabular interchange representation,
each AnnotationProperty has a corresponding table of Annotations

## OML AnnotationSubjectPropertyValue

For a given annotated OML TerminologyThing key,
an OML AnnotationSubjectPropertyValue is a pair:
- an annotation property
- an annotation value

## OML AnnotationSubjectTable

In a given OML TerminologyBox, annotations are indexed by
an OML TerminologyThing subject (key).
A subject (key) is associated to a table of OML AnnotationSubjectPropertyValues

## OML AnonymousConceptTaxonomyAxiom

Concrete, with 2 generalizations:
 - OML ConceptTreeDisjunction
 - OML DisjointUnionOfConceptsAxiom
An OML AnonymousConceptTaxonomyAxiom is an anonymous taxonomy tree of DisjointUnionOfEntityAxioms.

## OML Aspect

Concrete, with 2 generalizations:
 - OML Entity
 - OML UnaryTermKind
An OML Aspect ...

## OML AspectSpecializationAxiom

Concrete, with 1 generalization:
 - OML SpecializationAxiom
An OML AspectSpecializationAxiom ...

## OML Axiom

Abstract, with 1 generalization:
 - OML TerminologyBoxStatement
and with 2 specializations:
 - OML ScalarOneOfLiteralAxiom
 - OML TermAxiom
An OML Axiom ...

## OML BinaryScalarRestriction

Concrete, with 1 generalization:
 - OML RestrictedDataRange
An OML BinaryScalarRestriction is a data range that specifies how one binary scalar adds facet restrictions to another.
Applies when the restricted scalar represents binary data (OWL2: 4.5)
i.e., when it is one of the following scalars (or their transitively restricted ones):
xsd:hexBinary
xsd:base64Binary
xsd:minLength, xsd:maxLength, and xsd:length

## OML Bundle

Concrete, with 1 generalization:
 - OML TerminologyBox
A Bundle is a concrete TerminologyBox that is
an acyclic logical aggregate of other TerminologyBoxes (see TerminologyBundleAxiom)
and that can assert concept disjunctions (See TerminologyBundleStatement)

## OML BundledTerminologyAxiom

Concrete, with 1 generalization:
 - OML TerminologyBundleAxiom
An OML BundledTerminologyAxiom identifies an OML TerminologyBox that an OML Bundle aggregates.
An OML BundledTerminologyAxiom allows an OML Bundle to
make references (via OML TerminologyStatements) to OML TerminologyThings
within the transitive closure of a bundledTerminology.

## OML Concept

Concrete, with 3 generalizations:
 - OML ConceptualEntity
 - OML Entity
 - OML UnaryTermKind
An OML Concept ...

## OML ConceptDesignationTerminologyAxiom

Concrete, with 1 generalization:
 - OML TerminologyBoxAxiom
An OML ConceptDesignationTerminologyAxiom ...

## OML ConceptInstance

Concrete, with 1 generalization:
 - OML ConceptualEntitySingletonInstance
An OML ConceptInstance ...

## OML ConceptSpecializationAxiom

Concrete, with 1 generalization:
 - OML SpecializationAxiom
An OML ConceptSpecializationAxiom ...

## OML ConceptTreeDisjunction

Abstract, with 2 specializations:
 - OML AnonymousConceptTaxonomyAxiom
 - OML RootConceptTaxonomyAxiom
An OML ConceptTreeDisjunction represents the root & non-leaf nodes of a concept taxonomy:
- Root node is a RootConceptTaxonomyAxiom.
- Non-leaf nodes are AnonymousConceptTaxonomyAxioms.

## OML ConceptualEntity

Abstract, with 2 specializations:
 - OML Concept
 - OML ReifiedRelationship

## OML ConceptualEntitySingletonInstance

Abstract, with 1 generalization:
 - OML SingletonInstance
and with 2 specializations:
 - OML ConceptInstance
 - OML ReifiedRelationshipInstance
An OML ConceptualEntitySingletonInstance ...

## OML DataRange

Abstract, with 1 generalization:
 - OML Datatype
and with 2 specializations:
 - OML RestrictedDataRange
 - OML Scalar
An OWL DataRange corresponds to an OWL2 DataRange with arity=1.

## OML DataRelationship

Abstract, with 2 generalizations:
 - OML DirectedBinaryRelationshipKind
 - OML Term
and with 4 specializations:
 - OML EntityScalarDataProperty
 - OML EntityStructuredDataProperty
 - OML ScalarDataProperty
 - OML StructuredDataProperty
An OML DataRelationship ...

## OML DataRelationshipDomain

Abstract, with 2 specializations:
 - OML DataRelationshipFromEntity
 - OML DataRelationshipFromStructure
An OML DataRelationshipDomain ...

## OML DataRelationshipFromEntity

Abstract, with 1 generalization:
 - OML DataRelationshipDomain
and with 2 specializations:
 - OML EntityScalarDataProperty
 - OML EntityStructuredDataProperty
An OML DataRelationshipFromEntity defines a binary relationship
from an OML Entity domain to an OML Datatype of some kind.
The mapping of an OML DataRelationshipFromEntity to [OWL2-DL]
depends on the kind of OML Datatype.
The semantics of an OML DataRelationshipFromEntity to [OWL2-DL]
depends on whether it is an identity criteria for its OML Entity domain.

## OML DataRelationshipFromStructure

Abstract, with 1 generalization:
 - OML DataRelationshipDomain
and with 2 specializations:
 - OML ScalarDataProperty
 - OML StructuredDataProperty
An OML DataRelationshipFromStructure ...

## OML DataRelationshipRange

Abstract, with 2 specializations:
 - OML DataRelationshipToScalar
 - OML DataRelationshipToStructure
An OML DataRelationshipRange ...

## OML DataRelationshipToScalar

Abstract, with 1 generalization:
 - OML DataRelationshipRange
and with 2 specializations:
 - OML EntityScalarDataProperty
 - OML ScalarDataProperty
An OML DataRelationshipToScalar ...

## OML DataRelationshipToStructure

Abstract, with 1 generalization:
 - OML DataRelationshipRange
and with 2 specializations:
 - OML EntityStructuredDataProperty
 - OML StructuredDataProperty
An OML DataRelationshipToStructure ...

## OML DataStructureTuple

Concrete, with 1 generalization:
 - OML SingletonInstance
An OML DataStructureTuple ...

## OML Datatype

Abstract, with 2 generalizations:
 - OML Term
 - OML UnaryTermKind
and with 2 specializations:
 - OML DataRange
 - OML Structure
An OML Datatype ...

## OML DescriptionBox

Concrete, with 2 generalizations:
 - OML Resource
 - OML TerminologyThing
An OML DescriptionBox ...

## OML DescriptionBoxExtendsClosedWorldDefinitions

Concrete, with 1 generalization:
 - OML TerminologyThing
An OML DescriptionBoxExtendsClosedWorldDefinitions ...

## OML DescriptionBoxRefinement

Concrete, with 1 generalization:
 - OML TerminologyThing
An OML DescriptionBoxRefinement ...

## OML DirectedBinaryRelationshipKind

Abstract, with 2 specializations:
 - OML DataRelationship
 - OML EntityRelationship
An OML DirectedBinaryRelationshipKind ...

## OML DisjointUnionOfConceptsAxiom

Abstract, with 1 generalization:
 - OML TerminologyBundleStatement
and with 2 specializations:
 - OML AnonymousConceptTaxonomyAxiom
 - OML SpecificDisjointConceptAxiom
An OML DisjointUnionOfConceptsAxioms represents non-leaf & leaf nodes of a concept taxonomy:
- Non-leaf nodes are AnonymousConceptTaxonomyAxioms.
- Leaf nodes are SpecificDisjointConceptAxioms.

## OML Entity

Abstract, with 1 generalization:
 - OML Term
and with 3 specializations:
 - OML Aspect
 - OML Concept
 - OML ReifiedRelationship
An OML Entity ...

## OML EntityExistentialRestrictionAxiom

Concrete, with 1 generalization:
 - OML EntityRestrictionAxiom
An OML EntityExistentialRestrictionAxiom ...

## OML EntityRelationship

Abstract, with 2 generalizations:
 - OML DirectedBinaryRelationshipKind
 - OML Term
and with 2 specializations:
 - OML ReifiedRelationship
 - OML UnreifiedRelationship
An OML EntityRelationship ...

## OML EntityRestrictionAxiom

Abstract, with 1 generalization:
 - OML TermAxiom
and with 2 specializations:
 - OML EntityExistentialRestrictionAxiom
 - OML EntityUniversalRestrictionAxiom
An OML EntityRestrictionAxiom ...

## OML EntityScalarDataProperty

Concrete, with 3 generalizations:
 - OML DataRelationship
 - OML DataRelationshipFromEntity
 - OML DataRelationshipToScalar
An OML EntityScalarDataProperty ...

## OML EntityScalarDataPropertyExistentialRestrictionAxiom

Concrete, with 1 generalization:
 - OML EntityScalarDataPropertyRestrictionAxiom
An OML EntityScalarDataPropertyExistentialRestrictionAxiom maps to an
OWL2 DataSomeValuesFrom restriction (the range must be explicitly defined as a Scalar datatype)

## OML EntityScalarDataPropertyParticularRestrictionAxiom

Concrete, with 1 generalization:
 - OML EntityScalarDataPropertyRestrictionAxiom
*
An OML EntityScalarDataPropertyParticularRestrictionAxiom maps to an OWL2 DataHasValue restriction.

## OML EntityScalarDataPropertyRestrictionAxiom

Abstract, with 1 generalization:
 - OML TermAxiom
and with 3 specializations:
 - OML EntityScalarDataPropertyExistentialRestrictionAxiom
 - OML EntityScalarDataPropertyParticularRestrictionAxiom
 - OML EntityScalarDataPropertyUniversalRestrictionAxiom
Semantics: OWL2 Data Property Restrictions

## OML EntityScalarDataPropertyUniversalRestrictionAxiom

Concrete, with 1 generalization:
 - OML EntityScalarDataPropertyRestrictionAxiom
An OML EntityScalarDataPropertyUniversalRestrictionAxiom maps to an
OWL2 DataAllValuesFrom (the range must be explicitly defined as a Scalar datatype)

## OML EntityStructuredDataProperty

Concrete, with 3 generalizations:
 - OML DataRelationship
 - OML DataRelationshipFromEntity
 - OML DataRelationshipToStructure
An OML EntityStructuredDataProperty ...

## OML EntityUniversalRestrictionAxiom

Concrete, with 1 generalization:
 - OML EntityRestrictionAxiom
An OML EntityUniversalRestrictionAxiom ...

## OML IRIScalarRestriction

Concrete, with 1 generalization:
 - OML RestrictedDataRange
An OML IRIScalarRestriction is a data range that specifies how one IRI scalar adds facet restrictions to another.
Applies when the restricted scalar represents IRIs (OWL2: 4.6)
i.e., when it is one of the following scalars (or their transitively restricted ones):
xsd:anyURI

## OML NumericScalarRestriction

Concrete, with 1 generalization:
 - OML RestrictedDataRange
An OML NumericScalarRestriction is a data range that specifies how one numeric scalar range adds facet restrictions to another.
Applies when the restricted scalar represents real, decimal or integer numbers (OWL2: 4.1/4.2)
i.e., when it is one of the following scalars (or their transitively restricted ones):
owl:real
owl:rational
xsd:decimal
xsd:integer
xsd:nonNegativeInteger
xsd:nonPositiveInteger
xsd:positiveInteger
xsd:negativeInteger
xsd:long
xsd:int
xsd:short
xsd:byte
xsd:unsignedLong
xsd:unsignedInt
xsd:unsignedShort
xsd:unsignedByte
xsd:double
xsd:float

## OML PlainLiteralScalarRestriction

Concrete, with 1 generalization:
 - OML RestrictedDataRange
An OML PlainLiteralScalarRestriction is a data range that specifies how one plain literal scalar adds facet restrictions to another.
Applies when the restricted scalar represents plain literals (OWL2: 4.3)
i.e., when it is one of the following scalars (or their transitively restricted ones):
rdf:PlainLiteral

## OML ReifiedRelationship

Concrete, with 3 generalizations:
 - OML ConceptualEntity
 - OML Entity
 - OML EntityRelationship
An OML ReifiedRelationship ...

## OML ReifiedRelationshipInstance

Concrete, with 1 generalization:
 - OML ConceptualEntitySingletonInstance
An OML ReifiedRelationshipInstance ...

## OML ReifiedRelationshipInstanceDomain

Concrete, with 1 generalization:
 - OML TerminologyInstanceAssertion
An OML ReifiedRelationshipInstanceDomain ...

## OML ReifiedRelationshipInstanceRange

Concrete, with 1 generalization:
 - OML TerminologyInstanceAssertion
An OML ReifiedRelationshipInstanceRange ...

## OML ReifiedRelationshipSpecializationAxiom

Concrete, with 1 generalization:
 - OML SpecializationAxiom
An OML ReifiedRelationshipSpecializationAxiom ...

## OML Resource

Abstract, with 4 specializations:
 - OML DescriptionBox
 - OML SingletonInstance
 - OML Term
 - OML TerminologyBox
An OML Resource is an abstraction for
everything in a vocabulary that is identifiable
locally by name within the vocabulary and
globally by an IRI across multiple vocabularies.
For a particular OML Resource, the constraints
between its name and its IRI depend on what kind of OML Resource it is.

## OML RestrictedDataRange

Abstract, with 1 generalization:
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
An OML RestrictedDataRange corresponds to an OWL2 DataRange defined in terms of some kind of restriction of some other OML DataRange.
Instead of arbitrary OWL2 FacetRestrictionAxioms as constructors of OWL2 DataRanges,
the specializations of RestrictedDataRange correspond to the allowed restrictions in OWL2-DL datatype maps.
Node that the vocabulary of XSD fundamental facets is not included in OWL2-DL, consequently,
there is no support in OML for specifying datatype restrictions involving XSD fundamental facets as well.
@see https://www.w3.org/TR/owl2-syntax/#Data_Ranges
@see https://www.w3.org/TR/owl2-syntax/#Datatype_Maps

## OML RootConceptTaxonomyAxiom

Concrete, with 2 generalizations:
 - OML ConceptTreeDisjunction
 - OML TerminologyBundleStatement
An OML RootConceptTaxonomyAxiom asserts that, in the context of a Bundle, a particular Entity
is the root of a taxonomy of specializations of that Entity.

## OML Scalar

Concrete, with 1 generalization:
 - OML DataRange
An OML Scalar corresponds to an OWL2 Declaration of a Datatype with arity=1.

## OML ScalarDataProperty

Concrete, with 3 generalizations:
 - OML DataRelationship
 - OML DataRelationshipFromStructure
 - OML DataRelationshipToScalar
An OML ScalarDataProperty ...

## OML ScalarDataPropertyValue

Concrete, with 1 generalization:
 - OML TerminologyInstanceAssertion
An OML ...

## OML ScalarOneOfLiteralAxiom

Concrete, with 1 generalization:
 - OML Axiom
An OML ScalarOneOfLiteralAxiom specifies a literal in a ScalarOneOfRestriction data range.

## OML ScalarOneOfRestriction

Concrete, with 1 generalization:
 - OML RestrictedDataRange
An OML ScalarOneOfRestriction is a data range that specifies how a scalar is a restricted set of literal values of another.
Semantics: OWL2 DataOneOf

## OML SingletonInstance

Abstract, with 2 generalizations:
 - OML Resource
 - OML TerminologyInstanceAssertion
and with 2 specializations:
 - OML ConceptualEntitySingletonInstance
 - OML DataStructureTuple
An OML SingletonInstance ...

## OML SpecializationAxiom

Abstract, with 1 generalization:
 - OML TermAxiom
and with 3 specializations:
 - OML AspectSpecializationAxiom
 - OML ConceptSpecializationAxiom
 - OML ReifiedRelationshipSpecializationAxiom
An OML SpecializationAxiom ...

## OML SpecificDisjointConceptAxiom

Concrete, with 1 generalization:
 - OML DisjointUnionOfConceptsAxiom
An OML SpecificDisjointConceptAxiom specifies a leaf in a taxonomy tree.

## OML StringScalarRestriction

Concrete, with 1 generalization:
 - OML RestrictedDataRange
An OML StringScalarRestriction is a data range that specifies how one string scalar adds facet restrictions to another.
Applies when the restricted scalar represents strings (OWL2: 4.3)
i.e., when it is one of the following scalars (or their transitively restricted ones):
xsd:string
xsd:normalizedString
xsd:token
xsd:language
xsd:Name
xsd:NCName
xsd:NMTOKEN
xsd:length, xsd:minLength, xsd:maxLength, xsd:pattern

## OML Structure

Concrete, with 1 generalization:
 - OML Datatype
An OML Structure would correspond to an OWL2 Declaration of a Datatype with arity > 1.
However, since OWL2 Datatypes in the [OWL2-DL] are restricted to have arity=1,
the OML mapping to [OWL2-DL] involves a pattern-based usage of an [OWL2-DL Class] to represent an OML Structure.
The arity corresponds to the cardinality of the set of ScalarDataProperty & StructuredDataProperty
relationships whose domain is this structure.

## OML StructuredDataProperty

Concrete, with 3 generalizations:
 - OML DataRelationship
 - OML DataRelationshipFromStructure
 - OML DataRelationshipToStructure
An OML StructuredDataProperty ...

## OML StructuredDataPropertyValue

Concrete, with 1 generalization:
 - OML TerminologyInstanceAssertion
An OML StructuredDataPropertyValue ...

## OML SynonymScalarRestriction

Concrete, with 1 generalization:
 - OML RestrictedDataRange
An OML SynonymScalarRestriction is a data range that is defined as a synonym for another (i.e. the restrictedRange).

## OML Term

Abstract, with 2 generalizations:
 - OML Resource
 - OML TerminologyBoxStatement
and with 4 specializations:
 - OML DataRelationship
 - OML Datatype
 - OML Entity
 - OML EntityRelationship
An OML Term ...

## OML TermAxiom

Abstract, with 1 generalization:
 - OML Axiom
and with 3 specializations:
 - OML EntityRestrictionAxiom
 - OML EntityScalarDataPropertyRestrictionAxiom
 - OML SpecializationAxiom
An OML TermAxiom ...

## OML TerminologyAxiom

Abstract, with 1 generalization:
 - OML TerminologyThing
and with 2 specializations:
 - OML TerminologyBoxAxiom
 - OML TerminologyBundleAxiom
An OML TerminologyAxiom is asserted in a TerminologyBox of some kind.

## OML TerminologyBox

Abstract, with 2 generalizations:
 - OML Resource
 - OML TerminologyThing
and with 2 specializations:
 - OML Bundle
 - OML TerminologyGraph
An OML TerminologyBox is a logical set of OML TerminologyBoxStatements defining the vocabulary
for a domain, possibly by reuse of other vocabularies via OML TerminologyBoxAxioms.
The semantics of an OML TerminologyBox domain-specific vocabulary is defined
by the mapping to [OWL2-DL] of the other vocabularies it reuses, if any, and
that of its OML TerminologyBoxAxioms and OML TerminologyBoxStatements
according to its OML TerminologyGraphKind.

## OML TerminologyBoxAxiom

Abstract, with 1 generalization:
 - OML TerminologyAxiom
and with 3 specializations:
 - OML ConceptDesignationTerminologyAxiom
 - OML TerminologyExtensionAxiom
 - OML TerminologyNestingAxiom
An OML TerminologyBoxAxiom is a TerminologyAxiom that asserts a logical statement about a Term.

## OML TerminologyBoxStatement

Abstract, with 1 generalization:
 - OML TerminologyStatement
and with 2 specializations:
 - OML Axiom
 - OML Term
An OML TerminologyBoxStatement ...

## OML TerminologyBundleAxiom

Abstract, with 1 generalization:
 - OML TerminologyAxiom
and with 1 specialization:
 - OML BundledTerminologyAxiom
An OML TerminologyBundleAxiom is a TerminologyAxiom that asserts a logical statement in the context of a Bundle.

## OML TerminologyBundleStatement

Abstract, with 1 generalization:
 - OML TerminologyStatement
and with 2 specializations:
 - OML DisjointUnionOfConceptsAxiom
 - OML RootConceptTaxonomyAxiom
An OML TerminologyBundleStatement ...

## OML TerminologyExtensionAxiom

Concrete, with 1 generalization:
 - OML TerminologyBoxAxiom
An OML TerminologyExtensionAxiom allows an extendingTerminology to
make references (via TerminologyStatements) to TerminologyThings
within the transitive closure of the extendedTerminlogy.

## OML TerminologyExtent

An OML TerminologyExtent ...

## OML TerminologyGraph

Concrete, with 1 generalization:
 - OML TerminologyBox
A TerminologyGraph is a kind of TerminologyBox with no statements our axioms involving Bundles.

## OML TerminologyInstanceAssertion

Abstract, with 1 generalization:
 - OML TerminologyThing
and with 6 specializations:
 - OML ReifiedRelationshipInstanceDomain
 - OML ReifiedRelationshipInstanceRange
 - OML ScalarDataPropertyValue
 - OML SingletonInstance
 - OML StructuredDataPropertyValue
 - OML UnreifiedRelationshipInstanceTuple
An OML TerminologyInstanceAssertion ...

## OML TerminologyNestingAxiom

Concrete, with 1 generalization:
 - OML TerminologyBoxAxiom
An OML TerminologyNestingAxiom ...

## OML TerminologyStatement

Abstract, with 1 generalization:
 - OML TerminologyThing
and with 2 specializations:
 - OML TerminologyBoxStatement
 - OML TerminologyBundleStatement
An OML TerminologyStatement ...

## OML TerminologyThing

Abstract, with 7 specializations:
 - OML DescriptionBox
 - OML DescriptionBoxExtendsClosedWorldDefinitions
 - OML DescriptionBoxRefinement
 - OML TerminologyAxiom
 - OML TerminologyBox
 - OML TerminologyInstanceAssertion
 - OML TerminologyStatement
An OML TerminologyThing is an abstraction for everything
in a vocabulary that is globally identified by a UUID.

## OML TimeScalarRestriction

Concrete, with 1 generalization:
 - OML RestrictedDataRange
An OML TimeScalarRestriction is a data range that specifies how one time scalar adds facet restrictions to another.
Applies when the restricted scalar represents time instants (OWL2: 4.7)
i.e., when it is one of the following scalars (or their transitively restricted ones):
xsd:dateTime
xsd:dateTimeStamp

## OML UnaryTermKind

Abstract, with 3 specializations:
 - OML Aspect
 - OML Concept
 - OML Datatype
An OML UnaryTermKind ...

## OML UnreifiedRelationship

Concrete, with 1 generalization:
 - OML EntityRelationship
An OML UnreifiedRelationship ...

## OML UnreifiedRelationshipInstanceTuple

Concrete, with 1 generalization:
 - OML TerminologyInstanceAssertion
An OML UnreifiedRelationshipInstanceTuple ...
