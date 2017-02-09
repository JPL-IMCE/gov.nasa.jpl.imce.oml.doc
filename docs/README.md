{% include "./external-links.md" %}

# Ontological Modeling Language Specification

  
The Ontological Modeling Language, OML, is a thin vocabulary extension of [W3C]'s [OWL 2 Web Ontology Language] designed to support precise and scalable reasoning about descriptive systems engineering models.

## Vocabularies for Model-Based Systems Engineering

### What is a vocabulary?

Quote from [W3C's SemanticWeb summary:](https://www.w3.org/standards/semanticweb/ontology#summary "What is a vocabulary?")
> On the Semantic Web, vocabularies define the concepts and relationships (also referred to as “terms”) used to describe and represent an area of concern. Vocabularies are used to classify the terms that can be used in a particular application, characterize possible relationships, and define possible constraints on using those terms. 
In practice, vocabularies can be very complex (with several thousands of terms) or very simple (describing one or two concepts only). There is no clear division between what is referred to as “vocabularies” and “ontologies”. The trend is to use the word “ontology” for more complex, and possibly quite formal collection of terms, whereas “vocabulary” is used when such strict formalism is not necessarily used or only in a very loose sense. 
Vocabularies are the basic building blocks for inference techniques on the Semantic Web.

### The OML vocabulary is a subset of the [OWL2-DL] vocabulary

  

The core constructs of OML are:
  - [Terms](./Terms.md) such as concepts and relationships
  - [Axioms](./GLOSSARY.md#Axiom) about terms
  - [Terminologies](./GLOSSARY.md#Terminology), collections of terms & axioms

