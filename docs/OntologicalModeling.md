{% include "./external-links.md" %}

# Ontological Modeling

OML is designed to frame a rigorous approach for Model-Based Systems Engineering (MBSE).
From an MBSE perspective, a `model` in OML is an OML Context whose semantics is defined by
its mapping to an [OWL2-DL Ontology] with [SWRL] rules. This applies to different kinds
of `models` used in MBSE including but not limited to a metamodel like [OMG UML 2.5], 
a profile like [OMG SysML 1.4], a model library like SysML's QUDV and SysML's ISO-80000 library 
as well as user-defined models. From a pragmatic perspective, the semantics of 
an OML Context mapped from a UML/SysML `model` includes a formalization of SysML's `PropertySpecificType`;
a mechanism for describing a context-specific role that a SysML Block plays in the context of a system. 

The OML specification makes structural and semantic distinctions among three kinds of models,
each kind is an OML Context that maps to a particular usage of [OWL2-DL Ontology] with [SWRL] rules.

## Identification

OML uses the same identification principle than OWL2 for identifying OML Context(s) (i.e. [OWL2-DL Ontologies])
and their elements. For additional precision, OML includes support for specifying that an OML EntityDataProperty
has the semantics of an `IdentityCriteria` in the sense of [OntoClean] conveyed by the mapping to an [OWL2 Key Axiom].

## Annotations

OML Annotation(s) and OML AnnotationProperty(-ies) correspond, respectively, to [OWL2 Annotation] and [OWL2 AnnotationProperty].
Like [OWL2-DL], an OML Annotation is a non-logical axiom. Whereas [OWL2-DL] supports multiple levels of annotations (an [OWL2 Annotation] can be annotated);
OML supports a single level of annotation: an OML Annotation can only annotate an OML TerminologyThing subject.

An OML AnnotationProperty is identified by a combination of an abbreviated IRI and of an IRI. This allows using existing annotation vocabularies without explicitly importing them
(e.g., http://purl.org/dc/elements/1.1/).

## Ontologies

The notions of OML Context, OML Annotation, OML AnnotationProperty are described in the following figure:

![OML Contexts](images/OML Contexts.svg)

An OML Context maps to an [OWL2-DL Ontology] with a set of [OWL2 Axioms] and [SWRL] rules.
On first order, OML distinguishes between two kinds of OML Context(s):

- An OML TerminologyBox corresponds to a so-called [Tbox Ontology].

  There are two kinds of OML TerminologyBox(es):
  
  - `OpenWorldDefinitions`
  
  	This is for defining the vocabulary of a particular domain or for specializing a domain-specific vocabulary
  	for describing a usage of that vocabulary for modeling the types of parts and relationships that will be used
  	to in a `ClosedWorldDesignations` for designating distinct uses of these part & relationship types.
  	
  - `ClosedWorldDesignations`
  
  	This is for designating the individual parts and connections that constitute the topological structure of a system
  	described using `OpenWorldDefinitions` vocabularies.

  The key difference between these two kinds pertains the mapping to [OWL2 Class] of an OML ConceptualEntity and on an OML Structure.
  
  - In `OpenWorldDefinitions`, the mapping is per the usual open world semantics of [OWL2-DL] 
  	because the intent is precisely that of classifying an arbitrary set of individuals (or none).

  - In `ClosedWorldDesignations`, the mapping involves axioms that, effectively, force a singleton [OWL2 NamedIndividual]
  to represent a designated instance identified by the values of the OML EntityDataProperty(-ies) with `isIdentityCriteria=true`. This ensures
  that each designated instance is properly identified according to the criteria specified in the vocabulary and that topological and structural
  relationships at the instance level involve designated instances only. In other words, the topology and structure of a particular system
  is explicitly modeled in a `ClosedWorldDesignations` whereas it is only partially constrained in an `OpenWorldDefinitions`. 
  
  This distinction between the mapping of OML ConceptualEntity(-ies) and OML Structure(s) to [OWL2 Classes] provides opportunities
  for applying formal methods techniques to explore and refine possible topologies & structures of systems from partial descriptions.
  These techniques involve so-called *model finders*, such as:
  - the SAT-based [Kodkod] model finder for [Alloy]
  - the SMT-based [Formula] tool
  - in an unconventional albeit limited way, [OWL2-DL] reasoners such as [Pellet]
  
- An OML DesignationBox corresponds to a so-called [Abox Ontology].

	This is for describing a particular state of affairs about the individual designations of 
	the parts & relationships that describe the topology & structure of a particular system.
	A state of affairs is typically described via values of OML DataProperties.

## Organizing & Modularizing OML TerminologyBox(es)

OML distinguishes between two kinds of OML TerminologyBox(es):

- OML TerminologyGraph where the emphasis is on defining a domain-specific vocabulary or system-specific designations.

  Conceptually, it is useful to think about OML Concept(s) as defining the `nouns` of a vocabulary or of a system designation
  and about OML EntityRelationship(s) as defining `verbs` of a vocabulary or of a system designation. OML restricts a `verb` to
  be a directed relationship between a subject and an object that can be a `noun` or a reified `verb` (i.e. OML ReifiedRelationship).
 
  The purpose of an OML TerminologyGraph is to specify what is possible to describe in a domain-specific vocabulary or a system-specific
  designation and to support doing so in a modular, open-world fashion. That is, by defining an OML TerminologyGraph as an extension of another
  so that the former can use the vocabulary of the latter. Ontologies with open world semantics are essential for reusability and extensibility.
  This emphasis is reflected in the vocabulary of OML TerminologyGraph(s) in that their mapping to [OWL2 Ontologies] does not include any
  disjointness axioms for OML ConceptualEntity(-ies) -- i.e., [OWL2 Disjoint Classes Axiom] and [OWL2 Disjoint Union of Class Expressions Axiom].
  The principle behind this limitation is that a disjointness axiom represents an implicit closed-world assumption that all the distinctions
  of a particular [OWL2 Class] are known and can therefore be stated explicitly in such an axiom. OML provides support for this limited form
  of closed-world assumptions in OML Bundle(s).
  
  Although OML supports specialization of OML ConceptualEntities; it is generally preferable to convey context-specific restrictions on
  the domain/range of OML EntityRelationship(s) via restriction axioms rather than specialization, for example using OML EntityRestrictionAxiom(s)
  (existential or universal) thanks to the vocabulary of [OWL2 Object Property Restiction]. The rationale for this is that specialization
  augments the size of the vocabulary in a way that can dilute its meaning and utility. For example, consider a fititious domain-specific vocabulary 
  of vehicles sketched in OML textual concrete syntax as follows:
  
  ```OML
  open terminology http://www.example.org/vehicles {
 	abstract concept Vehicle
  	abstract concept Bicycle
  	abstract concept Car
  	abstract concept Train
  	Bicycle extendsConcept Vehicle
  	Car extendsConcept Vehicle
  	Train extendsConcept Vehicle
  }
  ```
  
  This vocabulary defines four OML Concept(s), `Vehicle`, `Bicycle`, `Car` and `Train`, organized in a simple taxonomy: `Vehicle` is a general
  concept with 3 specializations: `Bicycle`, `Car` and `Train`. From an OML perspective, the specializations are considered superfluous because
  there is no ontological distinction among them. In practice, it means that such a vocabulary does not provide users any support for
  answering legitimate questions about the intended purpose of the vocabulary nor what it actually means 
  (e.g., What is the difference between a `Bicycle` and a `Car`? What differentiates between a `Car` and a `Vehicle`?). 
  
  
  In this example, all four OML Concept(s) are defined nominally -- they are distinguishable only by their IRI.
  There is no ontologically significant distinction among them; which is a legitimate concern for rigorous modeling
  because the vocabulary provides no useful guidance for proper usage. To address this problem, the vocabulary would have
  to be augmented to include OML EntityRelationship(s) and/or OML DataRelationshipFromEntity(-ies) such that each OML Concept
  would have a distinguishable signature based on these relationships. 
  
  An OML TerminologyGraph vocabulary could be mapped to UML/SysML using class/block diagrams by mapping an OML Concept to a UML/SysML Class or Block
  and by mapping an OML EntityRelationship to a UML/SysML association. Note that an OML UnreifiedRelationship would map to a UML/SysML Association
  but an OML ReifiedRelationship would have to be mapped to a UML/SysML AssociationClass since it can play the role of a domain or a range 
  for an OML EntityRelationship of some kind that would be mapped to a UML/SysML Association or AssociationClass.
   Unfortunately, encoding equivalent restrictions
  for OML EntityRelationship(s) modeled as UML/SysML Associations of some kind requires specialization to use the UML mechanisms
  of association end subsetting and redefinition for encoding the intended context-specific restrictions. Regardless of mapping to UML/SysML,
  specializing OML EntityRelationship(s) for context-specific restrictions can lead to a substantial increase in the size of the domain-specific
  vocabulary because non-trivial domains typically require capturing many such restrictions. 
  
  Conversely, it is generally preferable to avoid superfluous specialization of OML Concept(s). In OML, a specialized OML Concept is superfluous
  unless the specialized OML Concept is involved in some kind of restriction on an OML EntityRelationship whose domain or range includes
  the parent OML Concept. For example, suppose that a fiticious domain-specific vocabulary of vehicles is defined as follows:
  
  TODO: elaborate a possible refinement...
  
  TODO: explain that non-superflous definitions provide important guidance for users because the signature of relationships
  associates to the OML Concept one or more patterns of usage.

- OML Bundle

### Canonical Parsing

The [OWL2 Structural Specification] defines the [Canonical Parsing of OWL2 Ontologies] 
from the concrete syntax representation of an ontology document 
(e.g., [OWL2 Functional Syntax], [OWL2 RDF/XML] and [OWL2 XML]) 
to an [OWL2 Ontology] that is an instance of the abstract syntax defined by the [OWL2 Structural Specification].
This canonical parsing process is specified in terms of the criteria 
of [OWL2 Structural Equivalence] and of the UML class diagrams that define the [OWL2 Structural Specification].

OML adopts a similar strategy; however, in lieu of using a very simple form UML class diagrams, 
the OML specification is the basis for generating a normalized relational database schema
(see the [concrete schema definitions of OML](GLOSSARY.md#oml-schema-concrete-glossary)). 

This normalized schema is designed to ensure that structurally equivalent OML Context(s) 
have identical representations in terms of instance data of the normalized schema.
Since an OML Context maps to an [OWL2 Ontology] and that a given [OWL2 Ontology] can be serialized
in multiple documents that are structurally equivalent to each other, it follows
that a given OML Context is structurally equivalent to all the serializations of ontology documents
that are structurally equivalent to its corresponding [OWL2 Ontology].
This propety is particularly important for change management because the OML normalized schema table
serialization ensures that any change in serialization is structurally significant by definition.
In contrast, change management with the serialization of OML Context(s) based on their mapping to [OWL2 Ontologies] 
would involve comparing serializations of ontology documents; such as [OWL2 RDF/XML], which is notorious for
allowing syntactically different serializations for structurally equivalent ontologies. 
This suggests that it is practically preferable to use the OML normalized schema table serialization
under change management because any change in serialization is structurally significant and use OML converters
to produce [OWL2 Ontology] documents as needed for [OWL2-DL] reasoning. 
