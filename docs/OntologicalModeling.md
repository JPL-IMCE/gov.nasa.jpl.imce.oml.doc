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

- An OML TerminologyBox corresponds to a so-called [Tbox Ontology] for defining the vocabulary of a particular domain or the description of a system using domain-specific vocabularies.

  The distinction between definitions and descriptions corresponds to the kind of OML TerminologyBox: `OpenWorldDefinitions` vs `ClosedWorldDesignations` respectively.
  
- An OML DesignationBox corresponds to a so-called [Abox Ontology] : it defines individuals describing a particular state of affairs of a system described in a closed OML TerminologyBox.

### Canonical Parsing

The [OWL2 Structural Specification] defines the [Canonical Parsing of OWL2 Ontologies] from the concrete syntax representation of an ontology document 
(e.g., [OWL2 Functional Syntax], [OWL2 RDF/XML] and [OWL2 XML]) to an [OWL2 Ontology] that is an instance of the abstract syntax defined by the [OWL2 Structural Specification].
This canonical parsing process is specified in terms of the criteria of [OWL2 Structural Equivalence] and of the UML class diagrams that define the [OWL2 Structural Specification].

OML adopts a similar strategy; however, in lieu of using a very simple form UML class diagrams, the OML specification is used for generating a normalized relational database schema
whose tables correspond precisely to the [concrete definitions of OML](GLOSSARY.md#oml-concrete-glossary). 

 a set of normalized relational database schema tables.
This normalized schema is designed to ensure that structurally equivalent OML Context(s) have identical representations in terms of instance data of the normalized schema.
This strong property ensures that 


Similarly, OML has an abstract syntax and multiple concrete syntaxes.
The OML abstract syntax is written in the Eclipse Xcore language; however, through code generation, it has equivalent Application Programming Interfaces (API) for different languages/technologies.
The OML Xcore specification generates an Eclipse EMF/CDO API via the Eclipse Xcore framework.
Additional code generators produce two di

 distinction between concrete and abstract syntax for a language is important to 
The [OWL2 Structural Specification] distinguishes between a cothe concrete syntax of an ontology document (e.g., Functional Syntax, N-triples, OWL/XML, RDF/XML...) 
and the abstract syntax of an [OWL2 Ontology] per the structural specification.
