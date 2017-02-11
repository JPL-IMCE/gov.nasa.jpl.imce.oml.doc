{% include "./external-links.md" %}

# The category of OML Terms

Every OML Term can be categorized in two ways.

## Categorization as a kind of relation

Formally, every OML Term is a logical relationship of arity 1 or 2.

- An OML UnaryTermKind such as an OML Concept or 
  an OML Scalar defines a word intended for describing things 
  whose existence is independent of anything else describable using the vocabulary.
  
  For example, an OML Terminology for the domain of vehicle registrations 
  in the USA could define an OML Concept for `Vehicle` and 
  an OML Scalar for `LicensePlateNumber`. This vocabulary would allow systems 
  engineers to use make precise descriptions of state of affairs about `Vehicles` and 
  about `LicensePlateNumbers` independently of any other concern; including their material 
  existence.
  
- An OML DirectedBinaryRelationshipKind such as an OML ScalarDataProperty formalizes a verb word used for describing
  a relationship involving a subject and an object.

  The vehicle registration example above could include an OML ScalarDataProperty, `hasLicensePlateNumber` 
  with domain `Vehicle` and range `LicensePlateNumber`. 

## Categorization by identity criteria

The criteria for identifying an instance of an OML Term leads to the following categories:

- OML Term with intrinsic identity semantics

  An instance of an OML Term with intrinsic identity is uniquely identified via its [IRI].
  Different instances with the same [IRI] are can be replaced with 
  a structurally and logically equivalent single instance with that [IRI].

  OML Entity defines the abstract category of OML Terms with intrinsic identity:
    - OML Aspect for defining common characteristics that any kind of OML Entity can inherit.
    - OML Concept, a kind of OML UnaryTermKind.
    - OML ReifiedRelationship, a kind of OML DirectedBinaryRelationshipKind.
  
- OML Term with structural equivalence semantics

  An instance of an OML Term with structural equivalence does not have an intrinsic identity; instead,
  it is semantically equivalent to another instance that it is structurally equivalent to.
  Structural equivalence depends on the kind of OML Term:
  
  - OML DataType (OML DataRange and OML Structure), which have OML UnaryRelationshipKind.
  
  	Structural equivalence for an instance of an OML DataType is defined inductively according to the structure of the OML DataType.
  	
  	For an OML DataRange, an instance is an atomic value represented as a string; such instances are equivalent if they have the same
  	string representation.
  	
  	For an OML Structure, an instance is an OML DataStructureTuple; which maps to an [OWL2 NamedIndividual]. 
  	Distinct OML DataStructureTuples with different [OWL2 Entity] [IRI]s are structurally equivalent if they have
  	equivalent values for the OML DataRelationshipFromStructure properties defined on the OML Structure.
  	 
  - OML DataRelationshipFromStructure, a kind of OML DirectedBinaryRelationshipKind.
  
    OML DataRelationshipToScalar => ScalarDataPropertyValue
    OML DataRelationshipToStructure => StructuredDataPropertyValue
  
- Instance of an OML Term with equivalent reference semantics
	 
  - OML UnreifiedRelationshipInstanceTuple is an instance of an OML UnreifiedRelationship, a kind of OML DirectedBinaryRelationshipKind.
  
  	An OML UnreifiedRelationshipInstanceTuple maps to an [OWL2 NamedIndividual]. 
  	Distinct OML UnreifiedRelationshipInstanceTuples with different [OWL2 Entity] [IRI]s are structurally equivalent if they
  	refer to the same OML UnreifiedRelationship and the same instances of OML ConceptualEntity playing the role of
  	domain and range for the tuple.

  - ... 
  
## Combined Categorization

Combining the two categorizations yields a 2x2 matrix of OML Term categories as follows:

|Relationship Arity            		 |Intrinsic Identity            |Structural Equivalence 	|
|:-----------------------------------|:-----------------------------|:--------------------------|
|OML UnaryRelationship         		 |OML Aspect, OML Concept       |OML DataType		   		|
|OML DirectedBinaryRelationshipKind  |OML ReifiedRelationship       |OML UnreifiedRelationship  |

OML [data properties] fall in a 2x2 matrix according to their domain and range as follows:

|[data property]    	|range=OML DataRange            |range=OML Structure                |
|:----------------------|:------------------------------|:----------------------------------|
|domain=OML Entity      |OML EntityScalarDataProperty   |OML EntityStructuredDataProperty   |
|domain=OML Structure   |OML ScalarDataProperty         |OML StructuredDataProperty         |

An OML DataRange maps to an [OWL2 Data Range] as follows:

|OML DataRange                  |Corresponding [OWL2 Data Range]    |
|:------------------------------|:----------------------------------|
|OML Scalar                     |[OWL2 Datatype]     				|
|OML RestrictedDataRange        |[OWL2 Datatype Restriction]        |

OML defines several [restricted data ranges] according to the allowable facet restrictions for [OWL2 Datatype Maps] as follows:

|OML RestrictedDataRange    		|Restricted [OWL2 Datatypes]            | Allowed Restriction Facets or Axioms       |
|:----------------------------------|:--------------------------------------|--------------------------------------------|
|OML BinaryScalarRestriction      	|[xsd:hexBinary], [xsd:base64Binary]    |[xsd:length], [xsd:minLength], [xsd:maxLength]|
|OML IRIScalarRestriction         	|[xsd:anyURI]                           |[xsd:length], [xsd:minLength], [xsd:maxLength], [xsd:pattern]|
|OML NumericScalarRestriction     	|[owl:real], [owl:rational], [xsd:decimal], [xsd:integer], [xsd:nonNegativeInteger], [xsd:nonPositiveInteger], [xsd:positiveInteger], [xsd:negativeInteger], [xsd:long], [xsd:int], [xsd:short], [xsd:byte], [xsd:unsignedLong], [xsd:unsignedInt], [xsd:unsignedShort], [xsd:unsignedByte], [xsd:double], [xsd:float] |[xsd:minExclusive], [xsd:minInclusive], [xsd:maxExclusive], [xsd:maxInclusive]|
|OML PlainLiteralScalarRestriction	|[rdf:PlainLiteral]                     |[rdf:langRange], [xsd:length], [xsd:minLength], [xsd:maxLength], [xsd:pattern]|
|OML StringScalarRestriction      	|[xsd:Name], [xsd:NCName], [xsd:NMTOKEN],[xsd:language], [xsd:normalizedString], [xsd:string], [xsd:token] |[xsd:length], [xsd:minLength], [xsd:maxLength], [xsd:pattern]|
|OML TimeScalarRestriction        	|[xsd:dateTime], [xsd:dateTimeStamp]    |[xsd:minExclusive], [xsd:minInclusive], [xsd:maxExclusive], [xsd:maxInclusive]|
|OML SynonymScalarRestriction    	|Alias for another OML DataRange      |None|
|OML ScalarOneOfRestriction       	|Another OML DataRange                |Enumeration of OML ScalarOneOfLiteral|



