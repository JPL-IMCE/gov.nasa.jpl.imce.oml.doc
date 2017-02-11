{% include "./external-links.md" %}

# OML is an [external DSL] with [OWL2-DL] as the host language

The key characteristics between the [external DSL] and the host language are:

- The abstract syntax structure of OML is a restricted subset of the abstract syntax 
  structure of [OWL2-DL], which means that:

   - Every well-formed OML [terminology] has a corresponding external representation as a 
     well-formed [OWL2-DL ontology].
   - A proper subset of well-formed [OWL2-DL ontologies] correspond to well-formed OML [terminologies]. 

- OML defines a [normalized relational tabular schema] for the serialization and interchange 
  of OML [terminologies] with the following guarantees:

   - Every well-formed OML [terminology] has a unique serialization as an OML [tables.zip].

   - The structural difference between two well-formed OML [terminologies] is precisely the set 
     of rows that are added or deleted when comparing their OML [tables.zip] serializations.
     
   - Two well-formed OML [terminologies] are structurally equivalent if and only if
     their OML [tables.zip] serializations are identical.

   - Structurally different OML [terminologies] have external representations as [OWL2-DL] ontologies
     that are structurally different per [OWL2-DL] regardless of the normative serialization 
     used, such as [OWL2 Functional Syntax], [OWL2 RDF/XML], [OWL2 XML].

- The semantics of an OML [terminology] is defined inductively by the structural mapping 
  to the host language, in the following way:

    - An OML [terminology] maps to an [OWL2-DL ontology].

    - An OML [term] of some kind maps to a pattern of [OWL2 axioms] including an [OWL2 declaration] for an [OWL2 entity] corresponding to the OML [term].