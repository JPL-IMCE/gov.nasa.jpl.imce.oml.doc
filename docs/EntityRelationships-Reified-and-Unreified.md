{% include "./external-links.md" %}

# Entity Relationships: Reified and Unreified

As explained in the W3C note about defining [N-ary Relations], one commonly encounters a limitation in the [OWL2-DL] vocabulary
for modeling relationships that, according to some domain, ought to be n-ary instead of binary like [OWL2 Object Properties] or [OWL2 Data Properties].
There are several strategies for encoding an n-ary relation; the W3C note describes a pattern based on [Introducing a new class for a relation].

In OML, all entity relationships are binary (n=2). 
On surface, it seems that reification would be unecessary since [OWL2 Object Properties] and [OWL2 Data Properties] are binary.
However, [OWL2] properties are binary and *unreified*; that is, neither an [OWL2 Object Property] nor an [OWL2 Data Property]
can be used as the domain or range of another [OWL2 Object Property] or [OWL2 Data Property] as this would violate the [Typing Constraints of OWL 2 DL]
unless [OWL2 Metamodeling] techniques are used; which effectively means that an IRI would be used for declaring, for example, 
an [OWL2 Object Property] and an [OWL2 Class], thereby allowing the same IRI to be used to refer to the [OWL2 Class] -- e.g., for classification --
or to the [OWL2 Object Property] -- e.g. for specifying or restricting its domain/range.

OML ReifiedRelationship is based on a variant of the [N-ary Relations Use-Case 1] encoded in [OWL2-DL] with [SWRL] rules without [OWL2 Metamodeling]
in full compliance with the [Global Restrictions on Axioms in OWL2 DL] including the restrictions on [OWL2 Property Hierarchy and Simple Object Property Expressions].
As [described in the summary](README.md#separation-of-assertions-and-entailments), 
this pattern presents a practically useful benefit because it enforces a complete separation
at the *instance* level between OML ReifiedRelationship(s) whose *instances* must be authored by someone because they require specifying an [OWL2 NamedIndividual]
and OML UnreifiedRelationship(s) whose *instances* can be inferred thanks to automated [OWL2 DL Reasoning] with [SWRL] rules (e.g., with the [Pellet] reasoner).

TODO ... diagram about theOML ReifiedRelationship pattern, explanation, examples ...
