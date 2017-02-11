{% include "./external-links.md" %}
# OML Glossary of 54 Concrete Definitions

## OML Annotation

An OML Annotation maps to an [OWL2 Annotation] and is similarly
a non-logical statement in an OML Context
associating some information as the value of an
OML AnnotationProperty for describing a subject (an OML TerminologyThing).

{APIs: **Functional**}

## OML AnnotationEntry

For the OML tabular interchange representation,
an OML AnnotationEntry (for a given OML AnnotationProperty) is a triple:
- an OML Context in which the OML AnnotationEntry appears
- an annotated OML TerminologyThing subject
- a String value as the representation of some information
  about the subject in that context.

{APIs: **Normalized**, **Functional**, **EMF/CDO**}

## OML AnnotationProperty

An OML AnnotationProperty maps to an [OWL2 AnnotationProperty]
and is similarly a non-logical property for associating some information
to any OML TerminologyThing in an OML Context.

{APIs: **Normalized**, **Functional**, **EMF/CDO**}

## OML AnnotationPropertyTable

For the OML tabular interchange representation,
an OML AnnotationPropertyTable pairs an OML AnnotationProperty key
with a set of OML AnnotationEntry values.

{APIs: **Functional**}

## OML AnnotationSubjectPropertyValue

An OML AnnotationSubjectPropertyValue is an in-memory construct
pairing an OML AnnotationProperty with a String value.

{APIs: **Normalized**, **EMF/CDO**}

## OML AnnotationSubjectTable

An OML AnnotationSubjectTable is an in-memory construct
pairing an OML TerminologyThing subject key with a set
of OML AnnotationSubjectPropertyValue tuples.

{APIs: **Normalized**, **EMF/CDO**}

## OML AnonymousConceptTaxonomyAxiom

An OML AnonymousConceptTaxonomyAxiom is an anonymous taxonomy tree of DisjointUnionOfEntityAxioms.

{APIs: **Normalized**, **Functional**, **EMF/CDO**}

Concrete definition with 2 generalizations:
 - OML ConceptTreeDisjunction
 - OML DisjointUnionOfConceptsAxiom

## OML Aspect

An OML Aspect is a kind of OML Entity of OML UnaryTermKind.
It is intended to be used as a specialization parent
for one or more OML ConceptualEntity.

{APIs: **Normalized**, **Functional**, **EMF/CDO**}

Concrete definition with 2 generalizations:
 - OML Entity
 - OML UnaryTermKind

## OML AspectSpecializationAxiom

An OML AspectSpecializationAxiom is a logical axiom
about a taxonomic relationship between a specific OML Aspect
and a general OML Entity.

{APIs: **Normalized**, **Functional**, **EMF/CDO**}

Concrete definition with 1 generalization:
 - OML SpecializationAxiom

## OML BinaryScalarRestriction

An OML BinaryScalarRestriction is a data range that specifies how one binary scalar adds facet restrictions to another.
Applies when the restricted scalar represents binary data (OWL2: 4.5)

The restricted scalar must be directly or indirectly a restriction of:
- [xsd:base64Binary]
- [xsd:hexBinary]

Facets:
- [xsd:length]
- [xsd:minLength]
- [xsd:maxLength]

{APIs: **Normalized**, **Functional**, **EMF/CDO**}

Concrete definition with 1 generalization:
 - OML RestrictedDataRange

## OML Bundle

An OML Bundle is an OML TerminologyBox that is
an acyclic logical aggregate of other OML TerminologyBoxes
and that logically assert OML TerminologyBundleStatements.

{APIs: **Normalized**, **Functional**, **EMF/CDO**}

Concrete definition with 1 generalization:
 - OML TerminologyBox

## OML BundledTerminologyAxiom

An OML BundledTerminologyAxiom identifies an OML TerminologyBox that an OML Bundle aggregates.
An OML BundledTerminologyAxiom allows an OML Bundle to
make references (via OML TerminologyStatements) to OML TerminologyThings
within the transitive closure of a bundledTerminology.

{APIs: **Normalized**, **Functional**, **EMF/CDO**}

Concrete definition with 1 generalization:
 - OML TerminologyBundleAxiom

## OML Concept

An OML Concept is an OML ConceptualEntity of OML UnaryTermKind.

{APIs: **Normalized**, **Functional**, **EMF/CDO**}

Concrete definition with 3 generalizations:
 - OML ConceptualEntity
 - OML Entity
 - OML UnaryTermKind

## OML ConceptDesignationTerminologyAxiom

An OML ConceptDesignationTerminologyAxiom establishes
a relationship from a source OML TerminologyBox
where a designated OML Concept is defined to
a target OML TerminologyGraph in which the internal
structure of the designated OML Concept can be defined.

{APIs: **Normalized**, **Functional**, **EMF/CDO**}

Concrete definition with 1 generalization:
 - OML TerminologyBoxAxiom

## OML ConceptInstance

An OML ConceptInstance is an OML ConceptualEntitySingletonInstance classified by an OML Concept.

{APIs: **Normalized**, **Functional**, **EMF/CDO**}

Concrete definition with 1 generalization:
 - OML ConceptualEntitySingletonInstance

## OML ConceptSpecializationAxiom

An OML ConceptSpecializationAxiom is a logical axiom
about a taxonomic relationship between a specific and general
OML Concept.

{APIs: **Normalized**, **Functional**, **EMF/CDO**}

Concrete definition with 1 generalization:
 - OML SpecializationAxiom

## OML DataStructureTuple

An OML DataStructureTuple defines an structured tuple instance of an OML Structure.

{APIs: **Normalized**, **Functional**, **EMF/CDO**}

Concrete definition with 1 generalization:
 - OML SingletonInstance

## OML DescriptionBox

An OML DescriptionBox maps to an [OWL2-DL Ontology]
about [OWL2-DL NamedIndividuals] mapped from OML TerminologyInstanceAssertions.

{APIs: **Normalized**, **Functional**, **EMF/CDO**}

Concrete definition with 1 generalization:
 - OML Context

## OML DescriptionBoxExtendsClosedWorldDefinitions

An OML DescriptionBoxExtendsClosedWorldDefinitions specifies
an OML DirectedBinaryRelationshipKind from an OML DescriptionBox
to an OML TerminologyBox such that an OML SingletonInstance defined in the
former can be an instance of an OML Term defined in the latter.

{APIs: **Normalized**, **Functional**, **EMF/CDO**}

Concrete definition with 2 generalizations:
 - OML DirectedBinaryRelationshipKind
 - OML TerminologyThing

## OML DescriptionBoxRefinement

An OML DescriptionBoxRefinement is an OML DirectedBinaryRelationshipKind
from an OML DescriptionBox to another OML DescriptionBox where
the former refines the descriptions of the latter.

{APIs: **Normalized**, **Functional**, **EMF/CDO**}

Concrete definition with 2 generalizations:
 - OML DirectedBinaryRelationshipKind
 - OML TerminologyThing

## OML EntityExistentialRestrictionAxiom

An OML EntityExistentialRestrictionAxiom maps
to an [OWL2 Object Property Existential Restriction].

{APIs: **Normalized**, **Functional**, **EMF/CDO**}

Concrete definition with 1 generalization:
 - OML EntityRestrictionAxiom

## OML EntityScalarDataProperty

An OML EntityScalarDataProperty is an OML DataRelationship
whose domain is an OML Entity and range is an OML DataRange.

{APIs: **Normalized**, **Functional**, **EMF/CDO**}

Concrete definition with 3 generalizations:
 - OML DataRelationship
 - OML DataRelationshipFromEntity
 - OML DataRelationshipToScalar

## OML EntityScalarDataPropertyExistentialRestrictionAxiom

An OML EntityScalarDataPropertyExistentialRestrictionAxiom maps to an
OWL2 DataSomeValuesFrom restriction (the range must be explicitly defined as a Scalar datatype)

{APIs: **Normalized**, **Functional**, **EMF/CDO**}

Concrete definition with 1 generalization:
 - OML EntityScalarDataPropertyRestrictionAxiom

## OML EntityScalarDataPropertyParticularRestrictionAxiom

*
An OML EntityScalarDataPropertyParticularRestrictionAxiom maps to an OWL2 DataHasValue restriction.

{APIs: **Normalized**, **Functional**, **EMF/CDO**}

Concrete definition with 1 generalization:
 - OML EntityScalarDataPropertyRestrictionAxiom

## OML EntityScalarDataPropertyUniversalRestrictionAxiom

An OML EntityScalarDataPropertyUniversalRestrictionAxiom maps to an
OWL2 DataAllValuesFrom (the range must be explicitly defined as a Scalar datatype)

{APIs: **Normalized**, **Functional**, **EMF/CDO**}

Concrete definition with 1 generalization:
 - OML EntityScalarDataPropertyRestrictionAxiom

## OML EntityStructuredDataProperty

An OML EntityStructuredDataProperty is an OML DataRelationship
whose domain is an OML Entity and range is an OML Structure.

{APIs: **Normalized**, **Functional**, **EMF/CDO**}

Concrete definition with 3 generalizations:
 - OML DataRelationship
 - OML DataRelationshipFromEntity
 - OML DataRelationshipToStructure

## OML EntityUniversalRestrictionAxiom

An OML EntityUniversalRestrictionAxiom maps
to an [OWL2 Object Property Universal Restriction].

{APIs: **Normalized**, **Functional**, **EMF/CDO**}

Concrete definition with 1 generalization:
 - OML EntityRestrictionAxiom

## OML IRIScalarRestriction

An OML IRIScalarRestriction is a data range that specifies how one IRI scalar adds facet restrictions to another.
Applies when the restricted scalar represents IRIs (OWL2: 4.6)

The restricted scalar must be directly or indirectly a restriction of:
- [xsd:anyURI]

Facets:
- [xsd:length]
- [xsd:minLength]
- [xsd:maxLength]
- [xsd:pattern]

{APIs: **Normalized**, **Functional**, **EMF/CDO**}

Concrete definition with 1 generalization:
 - OML RestrictedDataRange

## OML NumericScalarRestriction

An OML NumericScalarRestriction is a data range that specifies how one numeric scalar range adds facet restrictions to another.
Applies when the restricted scalar represents real, decimal or integer numbers (OWL2: 4.1/4.2)

The restricted scalar must be directly or indirectly a restriction of:
- [owl:real]
- [owl:rational]
- [xsd:decimal]
- [xsd:integer]
- [xsd:nonNegativeInteger]
- [xsd:nonPositiveInteger]
- [xsd:positiveInteger]
- [xsd:negativeInteger]
- [xsd:long]
- [xsd:int]
- [xsd:short]
- [xsd:byte]
- [xsd:unsignedLong]
- [xsd:unsignedInt]
- [xsd:unsignedShort]
- [xsd:unsignedByte]
- [xsd:double]
- [xsd:float]

Facets:
- [xsd:minInclusive]
- [xsd:maxInclusive]
- [xsd:minExclusive]
- [xsd:maxExclusive]

{APIs: **Normalized**, **Functional**, **EMF/CDO**}

Concrete definition with 1 generalization:
 - OML RestrictedDataRange

## OML PlainLiteralScalarRestriction

An OML PlainLiteralScalarRestriction is a data range that specifies how one plain literal scalar adds facet restrictions to another.
Applies when the restricted scalar represents plain literals (OWL2: 4.3)

The restricted scalar must be directly or indirectly a restriction of:
- [rdf:PlainLiteral]

Facets:
- [xsd:langRange]
- [xsd:length]
- [xsd:minLength]
- [xsd:maxLength]
- [xsd:pattern]

{APIs: **Normalized**, **Functional**, **EMF/CDO**}

Concrete definition with 1 generalization:
 - OML RestrictedDataRange

## OML ReifiedRelationship

An OML ReifiedRelationship is an OML ConceptualEntity and a kind of OML EntityRelationship
where an instance has an intrinsic identity. This means that
an OML ReifiedRelationship can be involved as the domain or the
range of another OML EntityRelationship as well as the
domain of an OML DataRelationshipFromEntity.

{APIs: **Normalized**, **Functional**, **EMF/CDO**}

Concrete definition with 3 generalizations:
 - OML ConceptualEntity
 - OML Entity
 - OML EntityRelationship

## OML ReifiedRelationshipInstance

An OML ReifiedRelationshipInstance is an OML ConceptualEntitySingletonInstance  classified by an OML ReifiedRelationship.

{APIs: **Normalized**, **Functional**, **EMF/CDO**}

Concrete definition with 1 generalization:
 - OML ConceptualEntitySingletonInstance

## OML ReifiedRelationshipInstanceDomain

An OML ReifiedRelationshipInstanceDomain specifies which OML ConceptualEntitySingletonInstance
plays the role of the domain for an OML ReifiedRelationshipInstance.
An OML ReifiedRelationshipInstanceDomain has no intrinsic identity; instead,
an OML ReifiedRelationshipInstanceDomain is semantically equivalent
to another OML ReifiedRelationshipInstanceDomain referencing the same property and domain.

{APIs: **Normalized**, **Functional**, **EMF/CDO**}

Concrete definition with 1 generalization:
 - OML TerminologyInstanceAssertion

## OML ReifiedRelationshipInstanceRange

An OML ReifiedRelationshipInstanceRange specifies which OML ConceptualEntitySingletonInstance
plays the role of the range for an OML ReifiedRelationshipInstance.
An OML ReifiedRelationshipInstanceRange has no intrinsic identity; instead,
an OML ReifiedRelationshipInstanceRange is semantically equivalent
to another OML ReifiedRelationshipInstanceRange referencing the same property and range.

{APIs: **Normalized**, **Functional**, **EMF/CDO**}

Concrete definition with 1 generalization:
 - OML TerminologyInstanceAssertion

## OML ReifiedRelationshipSpecializationAxiom

An OML ReifiedRelationshipSpecializationAxiom is a logical axiom
about a taxonomic relationship between a specific and general
OML ReifiedRelationship.

{APIs: **Normalized**, **Functional**, **EMF/CDO**}

Concrete definition with 1 generalization:
 - OML SpecializationAxiom

## OML RootConceptTaxonomyAxiom

An OML RootConceptTaxonomyAxiom asserts that, in the context of a Bundle, a particular Entity
is the root of a taxonomy of specializations of that Entity.

{APIs: **Normalized**, **Functional**, **EMF/CDO**}

Concrete definition with 2 generalizations:
 - OML ConceptTreeDisjunction
 - OML TerminologyBundleStatement

## OML Scalar

An OML Scalar corresponds to an OWL2 Declaration of a Datatype with arity=1.

{APIs: **Normalized**, **Functional**, **EMF/CDO**}

Concrete definition with 2 generalizations:
 - OML DataRange
 - OML UnaryTermKind

## OML ScalarDataProperty

An OML ScalarDataProperty is an OML DataRelationship
whose domain is an OML Structure and range is an OML DataRange.

{APIs: **Normalized**, **Functional**, **EMF/CDO**}

Concrete definition with 3 generalizations:
 - OML DataRelationship
 - OML DataRelationshipFromStructure
 - OML DataRelationshipToScalar

## OML ScalarDataPropertyValue

An OML ScalarDataPropertyValue defines a tuple for representing the atomic String value
of an OML DataRelationshipToScalar for a particular OML SingletonInstance.

{APIs: **Normalized**, **Functional**, **EMF/CDO**}

Concrete definition with 1 generalization:
 - OML TerminologyInstanceAssertion

## OML ScalarOneOfLiteralAxiom

An OML ScalarOneOfLiteralAxiom specifies a literal in a ScalarOneOfRestriction data range.

{APIs: **Normalized**, **Functional**, **EMF/CDO**}

Concrete definition with 1 generalization:
 - OML Axiom

## OML ScalarOneOfRestriction

An OML ScalarOneOfRestriction is a data range that specifies how a scalar is a restricted set of literal values of another.
Semantics: OWL2 DataOneOf

{APIs: **Normalized**, **Functional**, **EMF/CDO**}

Concrete definition with 1 generalization:
 - OML RestrictedDataRange

## OML SpecificDisjointConceptAxiom

An OML SpecificDisjointConceptAxiom specifies a leaf in a taxonomy tree.

{APIs: **Normalized**, **Functional**, **EMF/CDO**}

Concrete definition with 1 generalization:
 - OML DisjointUnionOfConceptsAxiom

## OML StringScalarRestriction

An OML StringScalarRestriction is a data range that specifies how one string scalar adds facet restrictions to another.
Applies when the restricted scalar represents strings (OWL2: 4.3)

The restricted scalar must be directly or indirectly a restriction of:
- [xsd:string]
- [xsd:normalizedString]
- [xsd:token]
- [xsd:language]
- [xsd:Name]
- [xsd:NCName]
- [xsd:NMTOKEN]

Facets:
- [xsd:length]
- [xsd:minLength]
- [xsd:maxLength]
- [xsd:pattern]

{APIs: **Normalized**, **Functional**, **EMF/CDO**}

Concrete definition with 1 generalization:
 - OML RestrictedDataRange

## OML Structure

An OML Structure would correspond to an OWL2 Declaration of a Datatype with arity > 1.
However, since OWL2 Datatypes in the [OWL2-DL] are restricted to have arity=1,
the OML mapping to [OWL2-DL] involves a pattern-based usage of an [OWL2-DL Class] to represent an OML Structure.
The arity corresponds to the cardinality of the set of ScalarDataProperty & StructuredDataProperty
relationships whose domain is this structure.

{APIs: **Normalized**, **Functional**, **EMF/CDO**}

Concrete definition with 2 generalizations:
 - OML Datatype
 - OML UnaryTermKind

## OML StructuredDataProperty

An OML StructuredDataProperty is an OML DataRelationship
whose domain is an OML Structure and range is an OML Structure.

{APIs: **Normalized**, **Functional**, **EMF/CDO**}

Concrete definition with 3 generalizations:
 - OML DataRelationship
 - OML DataRelationshipFromStructure
 - OML DataRelationshipToStructure

## OML StructuredDataPropertyValue

An OML StructuredDataPropertyValue defines a tuple for representing the structured tuple value
of an OML DataRelationshipToStructure for a particular OML SingletonInstance.

{APIs: **Normalized**, **Functional**, **EMF/CDO**}

Concrete definition with 1 generalization:
 - OML TerminologyInstanceAssertion

## OML SynonymScalarRestriction

An OML SynonymScalarRestriction is a data range that is defined as a synonym for another (i.e. the restrictedRange).

{APIs: **Normalized**, **Functional**, **EMF/CDO**}

Concrete definition with 1 generalization:
 - OML RestrictedDataRange

## OML TerminologyExtensionAxiom

An OML TerminologyExtensionAxiom allows an extendingTerminology to
make references (via TerminologyStatements) to TerminologyThings
within the transitive closure of the extendedTerminlogy.

{APIs: **Normalized**, **Functional**, **EMF/CDO**}

Concrete definition with 1 generalization:
 - OML TerminologyBoxAxiom

## OML TerminologyExtent

An OML TerminologyExtent defines an in-memory tuple
about all information pertaining to the use of OML
for modeling domain-specific vocabularies and
domain-specific descriptions of systems using such vocabularies.

{APIs: **Functional**}

## OML TerminologyGraph

An OML TerminologyGraph is an OML TerminologyBox with no statements our axioms involving OML Bundles.

{APIs: **Normalized**, **Functional**, **EMF/CDO**}

Concrete definition with 1 generalization:
 - OML TerminologyBox

## OML TerminologyNestingAxiom

An OML TerminologyNestingAxiom provides support for relating
a white-box OML TerminologyGraph as a nested terminology
providing details about a black-box OML Concept defined
in a nesting OML TerminologyBox.

{APIs: **Normalized**, **Functional**, **EMF/CDO**}

Concrete definition with 1 generalization:
 - OML TerminologyBoxAxiom

## OML TimeScalarRestriction

An OML TimeScalarRestriction is a data range that specifies how one time scalar adds facet restrictions to another.
Applies when the restricted scalar represents time instants (OWL2: 4.7)

The restricted scalar must be directly or indirectly a restriction of:
- [xsd:dateTime]
- [xsd:dateTimeStamp]

Facets:
- [xsd:minInclusive]
- [xsd:maxInclusive]
- [xsd:minExclusive]
- [xsd:maxExclusive]

{APIs: **Normalized**, **Functional**, **EMF/CDO**}

Concrete definition with 1 generalization:
 - OML RestrictedDataRange

## OML UnreifiedRelationship

An OML UnreifiedRelationship is a kind of OML EntityRelationship
where an instance has no intrinsic identity but rather structural
equivalence semantics as a tuple of references. This means
that an OML UnreifiedRelationship cannot be involved as the domain
or range of any kind of OML DirectedBinaryRelationshipKind.

{APIs: **Normalized**, **Functional**, **EMF/CDO**}

Concrete definition with 1 generalization:
 - OML EntityRelationship

## OML UnreifiedRelationshipInstanceTuple

An OML UnreifiedRelationshipInstanceTuple specifies a triple involving
a reference to an OML ConceptualEntitySingletonInstance playing the role of the domain
of an OML UnreifiedRelationship whose range is played by a reference to an OML ConceptualEntitySingletonInstance.
An OML UnreifiedRelationshipInstanceTuple has no intrinsic identity; instead,
an OML UnreifiedRelationshipInstanceTuple is semantically equivalent
to another OML UnreifiedRelationshipInstanceTuple referencing the same domain, property and range.

{APIs: **Normalized**, **Functional**, **EMF/CDO**}

Concrete definition with 1 generalization:
 - OML TerminologyInstanceAssertion
