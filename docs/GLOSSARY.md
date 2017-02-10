# Glossary

## OML Annotation

An OML Annotation ...

## OML AnnotationEntry

In the OML tabular interchange representation,
an AnnotationEntry (for a given AnnotationProperty) is a triple:
- the terminology in which the annotation appears
- the annotated terminology thing (subject)
- the value of the AnnotationProperty for that subject in that terminology

## OML AnnotationProperty

An OML AnnotationProperty ...

## OML AnnotationPropertyTable

For the OML tabular interchange representation,
each AnnotationProperty has a corresponding table of Annotations

## OML AnnotationSubjectPropertyValue

For a given annotated TerminologyThing key,
an AnnotationSubjectPropertyValue is a pair:
- an annotation property
- an annotation value

## OML AnnotationSubjectTable

In a given terminology, annotations are indexed by TerminologyThing subject (key).
A subject (key) is associated to a table of AnnotationSubjectPropertyValues

## OML AnonymousConceptTaxonomyAxiom

An OML AnonymousConceptTaxonomyAxiom is an anonymous taxonomy tree of DisjointUnionOfEntityAxioms.

## OML Aspect

An OML Aspect ...

## OML AspectSpecializationAxiom

An OML AspectSpecializationAxiom ...

## OML Axiom

An OML Axiom ...

## OML BinaryScalarRestriction

An OML BinaryScalarRestriction is a data range that specifies how one binary scalar adds facet restrictions to another.
Applies when the restricted scalar represents binary data (OWL2: 4.5)
i.e., when it is one of the following scalars (or their transitively restricted ones):
xsd:hexBinary
xsd:base64Binary
xsd:minLength, xsd:maxLength, and xsd:length

## OML Bundle

A Bundle is a concrete TerminologyBox that is
an acyclic logical aggregate of other TerminologyBoxes (see TerminologyBundleAxiom)
and that can assert concept disjunctions (See TerminologyBundleStatement)

## OML BundledTerminologyAxiom

An OML BundledTerminologyAxiom identifies an OML TerminologyBox that an OML Bundle aggregates.
An OML BundledTerminologyAxiom allows an OML Bundle to
make references (via OML TerminologyStatements) to OML TerminologyThings
within the transitive closure of a bundledTerminology.

## OML Concept

An OML Concept ...

## OML ConceptDesignationTerminologyAxiom

An OML ConceptDesignationTerminologyAxiom ...

## OML ConceptInstance

An OML ConceptInstance ...

## OML ConceptSpecializationAxiom

An OML ConceptSpecializationAxiom ...

## OML ConceptTreeDisjunction

An OML ConceptTreeDisjunction represents the root & non-leaf nodes of a concept taxonomy:
- Root node is a RootConceptTaxonomyAxiom.
- Non-leaf nodes are AnonymousConceptTaxonomyAxioms.

## OML ConceptualEntity


## OML ConceptualEntitySingletonInstance

An OML ConceptualEntitySingletonInstance ...

## OML DataRange

An OWL DataRange corresponds to an OWL2 DataRange with arity=1.

## OML DataRelationship

An OML DataRelationship ...

## OML DataRelationshipDomain

An OML DataRelationshipDomain ...

## OML DataRelationshipFromEntity

An OML DataRelationshipFromEntity defines a binary relationship
from an OML Entity domain to an OML Datatype of some kind.
The mapping of an OML DataRelationshipFromEntity to [OWL2-DL]
depends on the kind of OML Datatype.
The semantics of an OML DataRelationshipFromEntity to [OWL2-DL]
depends on whether it is an identity criteria for its OML Entity domain.

## OML DataRelationshipFromStructure

An OML DataRelationshipFromStructure ...

## OML DataRelationshipRange

An OML DataRelationshipRange ...

## OML DataRelationshipToScalar

An OML DataRelationshipToScalar ...

## OML DataRelationshipToStructure

An OML DataRelationshipToStructure ...

## OML DataStructureTuple

An OML DataStructureTuple ...

## OML Datatype

An OML Datatype ...

## OML DescriptionBox

An OML DescriptionBox ...

## OML DescriptionBoxExtendsClosedWorldDefinitions

An OML DescriptionBoxExtendsClosedWorldDefinitions ...

## OML DescriptionBoxRefinement

An OML DescriptionBoxRefinement ...

## OML DirectedBinaryRelationshipKind

An OML DirectedBinaryRelationshipKind ...

## OML DisjointUnionOfConceptsAxiom

An OML DisjointUnionOfConceptsAxioms represents non-leaf & leaf nodes of a concept taxonomy:
- Non-leaf nodes are AnonymousConceptTaxonomyAxioms.
- Leaf nodes are SpecificDisjointConceptAxioms.

## OML Entity

An OML Entity ...

## OML EntityExistentialRestrictionAxiom

An OML EntityExistentialRestrictionAxiom ...

## OML EntityRelationship

An OML EntityRelationship ...

## OML EntityRestrictionAxiom

An OML EntityRestrictionAxiom ...

## OML EntityScalarDataProperty

An OML EntityScalarDataProperty ...

## OML EntityScalarDataPropertyExistentialRestrictionAxiom

An OML EntityScalarDataPropertyExistentialRestrictionAxiom maps to an
OWL2 DataSomeValuesFrom restriction (the range must be explicitly defined as a Scalar datatype)

## OML EntityScalarDataPropertyParticularRestrictionAxiom

*
An OML EntityScalarDataPropertyParticularRestrictionAxiom maps to an OWL2 DataHasValue restriction.

## OML EntityScalarDataPropertyRestrictionAxiom

Semantics: OWL2 Data Property Restrictions

## OML EntityScalarDataPropertyUniversalRestrictionAxiom

An OML EntityScalarDataPropertyUniversalRestrictionAxiom maps to an
OWL2 DataAllValuesFrom (the range must be explicitly defined as a Scalar datatype)

## OML EntityStructuredDataProperty

An OML EntityStructuredDataProperty ...

## OML EntityUniversalRestrictionAxiom

An OML EntityUniversalRestrictionAxiom ...

## OML IRIScalarRestriction

An OML IRIScalarRestriction is a data range that specifies how one IRI scalar adds facet restrictions to another.
Applies when the restricted scalar represents IRIs (OWL2: 4.6)
i.e., when it is one of the following scalars (or their transitively restricted ones):
xsd:anyURI

## OML NumericScalarRestriction

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

An OML PlainLiteralScalarRestriction is a data range that specifies how one plain literal scalar adds facet restrictions to another.
Applies when the restricted scalar represents plain literals (OWL2: 4.3)
i.e., when it is one of the following scalars (or their transitively restricted ones):
rdf:PlainLiteral

## OML ReifiedRelationship

An OML ReifiedRelationship ...

## OML ReifiedRelationshipInstance

An OML ReifiedRelationshipInstance ...

## OML ReifiedRelationshipInstanceDomain

An OML ReifiedRelationshipInstanceDomain ...

## OML ReifiedRelationshipInstanceRange

An OML ReifiedRelationshipInstanceRange ...

## OML ReifiedRelationshipSpecializationAxiom

An OML ReifiedRelationshipSpecializationAxiom ...

## OML Resource

An OML Resource ...

## OML RestrictedDataRange

An OML RestrictedDataRange corresponds to an OWL2 DataRange defined in terms of some kind of restriction of some other OML DataRange.
Instead of arbitrary OWL2 FacetRestrictionAxioms as constructors of OWL2 DataRanges,
the specializations of RestrictedDataRange correspond to the allowed restrictions in OWL2-DL datatype maps.
Node that the vocabulary of XSD fundamental facets is not included in OWL2-DL, consequently,
there is no support in OML for specifying datatype restrictions involving XSD fundamental facets as well.
@see https://www.w3.org/TR/owl2-syntax/#Data_Ranges
@see https://www.w3.org/TR/owl2-syntax/#Datatype_Maps

## OML RootConceptTaxonomyAxiom

An OML RootConceptTaxonomyAxiom asserts that, in the context of a Bundle, a particular Entity
is the root of a taxonomy of specializations of that Entity.

## OML Scalar

An OML Scalar corresponds to an OWL2 Declaration of a Datatype with arity=1.

## OML ScalarDataProperty

An OML ScalarDataProperty ...

## OML ScalarDataPropertyValue

An OML ...

## OML ScalarOneOfLiteralAxiom

An OML ScalarOneOfLiteralAxiom specifies a literal in a ScalarOneOfRestriction data range.

## OML ScalarOneOfRestriction

An OML ScalarOneOfRestriction is a data range that specifies how a scalar is a restricted set of literal values of another.
Semantics: OWL2 DataOneOf

## OML SingletonInstance

An OML SingletonInstance ...

## OML SpecializationAxiom

An OML SpecializationAxiom ...

## OML SpecificDisjointConceptAxiom

An OML SpecificDisjointConceptAxiom specifies a leaf in a taxonomy tree.

## OML StringScalarRestriction

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

An OML Structure would correspond to an OWL2 Declaration of a Datatype with arity > 1.
However, since OWL2 Datatypes in the [OWL2-DL] are restricted to have arity=1,
the OML mapping to [OWL2-DL] involves a pattern-based usage of an [OWL2-DL Class] to represent an OML Structure.
The arity corresponds to the cardinality of the set of ScalarDataProperty & StructuredDataProperty
relationships whose domain is this structure.

## OML StructuredDataProperty

An OML StructuredDataProperty ...

## OML StructuredDataPropertyValue

An OML StructuredDataPropertyValue ...

## OML SynonymScalarRestriction

An OML SynonymScalarRestriction is a data range that is defined as a synonym for another (i.e. the restrictedRange).

## OML Term

An OML Term ...

## OML TermAxiom

An OML TermAxiom ...

## OML TerminologyAxiom

An OML TerminologyAxiom is asserted in a TerminologyBox of some kind.

## OML TerminologyBox

An OML TerminologyBox is a logical set of OML TerminologyBoxStatements defining the vocabulary
for a domain, possibly by reuse of other vocabularies via OML TerminologyBoxAxioms.
The semantics of an OML TerminologyBox domain-specific vocabulary is defined
by the mapping to [OWL2-DL] of the other vocabularies it reuses, if any, and
that of its OML TerminologyBoxAxioms and OML TerminologyBoxStatements
according to its OML TerminologyGraphKind.

## OML TerminologyBoxAxiom

An OML TerminologyBoxAxiom is a TerminologyAxiom that asserts a logical statement about a Term.

## OML TerminologyBoxStatement

An OML TerminologyBoxStatement ...

## OML TerminologyBundleAxiom

An OML TerminologyBundleAxiom is a TerminologyAxiom that asserts a logical statement in the context of a Bundle.

## OML TerminologyBundleStatement

An OML TerminologyBundleStatement ...

## OML TerminologyExtensionAxiom

An OML TerminologyExtensionAxiom allows an extendingTerminology to
make references (via TerminologyStatements) to TerminologyThings
within the transitive closure of the extendedTerminlogy.

## OML TerminologyExtent

An OML TerminologyExtent ...

## OML TerminologyGraph

A TerminologyGraph is a kind of TerminologyBox with no statements our axioms involving Bundles.

## OML TerminologyGraphKind

OML supports two different interpretations for OML TerminologyBox vocabularies:
- An open-world interpretation where the vocabulary formalizes a particular domain
  that will be used for modeling particular systems in that domain.
- A closed-world interpretation where the vocabulary formalizes the description of
  a particular system modeled using the open-world vocabulary for a particular domain.
The difference between these interpretations primarily affects the mapping to an [OWL2-DL Class]
of a concrete OML ConceptualEntity as follows:
- For OpenWorldDefinitions, the mapped [OWL2-DL Class] has open-world semantics; that is,
  it classifies a set of individuals that share the characteristics and capabilities
  encoded in the [OWL2-DL Class].
- For ClosedWorldDefinitions, the mapped [OWL2-DL Class] has a closed-world semantics in
  the sense that it is intended to classify a singleton individual uniquely identified
  via the values of its identifying OML DataRelationshipFromEntity properties.

## OML TerminologyInstanceAssertion

An OML TerminologyInstanceAssertion ...

## OML TerminologyNestingAxiom

An OML TerminologyNestingAxiom ...

## OML TerminologyStatement

An OML TerminologyStatement ...

## OML TerminologyThing

An OML TerminologyThing ...

## OML TimeScalarRestriction

An OML TimeScalarRestriction is a data range that specifies how one time scalar adds facet restrictions to another.
Applies when the restricted scalar represents time instants (OWL2: 4.7)
i.e., when it is one of the following scalars (or their transitively restricted ones):
xsd:dateTime
xsd:dateTimeStamp

## OML UnaryTermKind

An OML UnaryTermKind ...

## OML UnreifiedRelationship

An OML UnreifiedRelationship ...

## OML UnreifiedRelationshipInstanceTuple

An OML UnreifiedRelationshipInstanceTuple ...
