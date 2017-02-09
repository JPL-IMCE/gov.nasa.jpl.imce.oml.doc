{% include "./external-links.md" %}
[term]: {glossary.path}#Term
[terms]: {glossary.path}#Term


### The category of OML [terms]

OML *terms* can be categorized in two ways.

#### Categorizing OML *terms* as relations

Formally, OML *terms* are logical relationships categorized by their arity as follows:

- An OML [unary relationship] such as an OML [concept] or 
  an OML [scalar] defines a word intended for describing things 
  whose existence is independent of anything else describable using the vocabulary.
  
  For example, an OML [terminology] for the domain of vehicle registrations 
  in the USA could define a [concept] for `Vehicle` and 
  a [scalar] for `LicensePlateNumber`. This vocabulary would allow systems 
  engineers to use make precise descriptions of state of affairs about `Vehicles` and 
  about `LicensePlateNumbers` independently of any other concern; including their material 
  existence.
  
- A [directed binary relationship] such as a [scalar data property] formalizes a verb word used for describing
  a relationship involving a subject and an object.

  The vehicle registration example above could include a [scalar data property], `hasLicensePlateNumber` 
  with domain `Vehicle` and range `LicensePlateNumber`. 

#### Categorizing OML *terms* by identity criteria

The criteria for identifying instances of OML *terms* leads to the following categories:

- OML *terms* with intrinsic identity semantics

  An instance of an OML [term] with intrinsic identity is uniquely identified via its [IRI].
  Different instances with the same [IRI] are can be replaced with 
  a structurally and logically equivalent single instance with that [IRI].

  OML [terms] with intrinsic identity is the category of OML [entities]:
    - OML [aspect] for defining common characteristics that any kind of OML [entity] can inherit.
    - OML [concept], a kind of OML [unary relationship].
    - OML [reified relationship], a kind of OML [directed binary relationship].
  
- OML *terms* with structural equivalence semantics

  An instance of an OML [term] with structural equivalence is identified by its structure.
  Different instances with equivalent structures can be replaced with 
  a structurally and logically equivalent single instance with that structure.
 
  OML [terms] with structural equivalence are:
  - OML [datatypes] ([scalar] and [structure]), which are kinds of OML [unary relationships].
  - OML [data properties], a kind of OML [directed binary relationship].
  - OML [unreified relationships], a kind of OML [directed binary relationship].

#### Categorizing OML *terms* by relation arity and by identity criteria

Combining the two categorizations yields a 2x2 matrix of OML *terms* as follows:

|Relationship Arity             |Intrinsic Identity            |Structural Equivalence |
|:------------------------------|:-----------------------------|:----------------------|
|[unary relationship]           |[aspect], [concept]           |[datarange], [structure]  |
|[directed binary relationship] |[reified relationship]        |[unreified relationship], [data properties]|

OML [data properties] fall in a 2x2 matrix according to their domain and range as follows:

|[data property]                |range=[datarange]              |range=[structure]                  |
|:------------------------------|:------------------------------|:----------------------------------|
|domain=[entity]                |[entity scalar data property]  |[entity structured data property]  |
|domain=[structure]             |[scalar data property]         |[structured data property]         |

OML [dataranges] map to [OWL2 data ranges] as follows:

|OML [datarange]                |Corresponding [OWL2 data range]    |
|:------------------------------|:----------------------------------|
|[scalar]                       |[OWL2 Datatype]       |
|[restricted data range]        |[OWL2 Datatype Restriction]        |

OML defines several [restricted data ranges] according to the allowable facet restrictions for [OWL2 Datatype Maps] as follows:

|OML [restricted data range]    |Restricted [OWL2 Datatypes]            | Allowed Restriction Facets or Axioms       |
|:------------------------------|:--------------------------------------|--------------------------------------------|
|[BinaryScalarRestriction]      |[xsd:hexBinary], [xsd:base64Binary]    |[xsd:length], [xsd:minLength], [xsd:maxLength]|
|[IRIScalarRestriction]         |[xsd:anyURI]                           |[xsd:length], [xsd:minLength], [xsd:maxLength], [xsd:pattern]|
|[NumericScalarRestriction]     |[owl:real], [owl:rational], [xsd:decimal], [xsd:integer], [xsd:nonNegativeInteger], [xsd:nonPositiveInteger], [xsd:positiveInteger], [xsd:negativeInteger], [xsd:long], [xsd:int], [xsd:short], [xsd:byte], [xsd:unsignedLong], [xsd:unsignedInt], [xsd:unsignedShort], [xsd:unsignedByte], [xsd:double], [xsd:float] |[xsd:minExclusive], [xsd:minInclusive], [xsd:maxExclusive], [xsd:maxInclusive]|
|[PlainLiteralScalarRestriction]|[rdf:PlainLiteral]                     |[rdf:langRange], [xsd:length], [xsd:minLength], [xsd:maxLength], [xsd:pattern]|
|[StringScalarRestriction]      |[xsd:Name], [xsd:NCName], [xsd:NMTOKEN],[xsd:language], [xsd:normalizedString], [xsd:string], [xsd:token] |[xsd:length], [xsd:minLength], [xsd:maxLength], [xsd:pattern]|
|[TimeScalarRestriction]        |[xsd:dateTime], [xsd:dateTimeStamp]    |[xsd:minExclusive], [xsd:minInclusive], [xsd:maxExclusive], [xsd:maxInclusive]|
|[SynonymScalarRestriction]     |Alias for another OML [datarange]      |None|
|[ScalarOneOfRestriction]       |Another OML [datarange]                |Enumeration of [ScalarOneOfLiteral]|



