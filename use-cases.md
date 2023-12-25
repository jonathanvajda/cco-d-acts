# CCO Document Acts Ontology Working Group (CODA WG)
This working group is to develop the theory and framework of Document Acts. Document Acts are processes which have ....

## Use Cases, Competency Questions, and Intended Knowledge Graphs
Each use case is framed in terms of a type of scenario and/or a competency question. A scenario may be a set of assertions (information about entities and their relationships). A compentency question is an informal (or semi-formal) question for which some data would return as an answer. The competency question is used as a benchmark for whether the representation is sufficiently expressive to be able to return the information in view. A set of competency questions can be used as a set of requirements for a tell-and-ask system supported with an ontology. The questions can be formalized in terms of a SPARQL query. The use case or the competency question may be diagramed with the relationships, made explicit in a visualization of a graph of individuals, classes, and object and data properties asserted in the model. If the visualization represents knowledge, it may be considered an "intended knowledge graph."

Progress in providing coverage is tracked with the checklist below (or with an issue tracker link). Every use case is considered "covered" when:
- the representation exemplifies or extends the Common Core Ontologies' design pattern(s)
- the CCO-conformant design pattern is documented (in Word, PowerPoint, or otherwise)
- there is a sample of data in view (real or merely notional)
- there is a visualization that captures a graph of that sample data according to the design pattern (draw.io, PowerPoint, Visio, or otherwise). This is called an "intended knowledge graph."
- there is an OWL2 ontology file (owl, ttl, rdf) with opaque IRIs in a Documents Acts namespace, with all resources properly annotated
- a sample SPARQL query that formalizes the competency question is drafted

## Annotation Requirements
| Annotation | AnnotationType | Restrictions|
|---|:---:|:---:|
| Unique term; unambiguous, zero-collision, future-proofed label | rdfs:label | exactly 1 per language, with a language tag |
| Domain specialists' or industry-standard technical term | skos:prefLabel | exactly 1 per language, with a language tag |
| Optional: if there is no consensus among specialists or there are competing industry standards, then provide alternatives | skos:altLabel | with a language tag |
| Person or group who initially created element | dcterms:creator | at least 1, expects a literal value |
| Time stamp when the element was created | dcterms:created | YYYY-MM-DD hh:mm:ss.sss with offset from UTC |
| Definition in Genus + Specific difference format (applies to classes and properties, not individuals) | skos:definition | exactly 1, with language tag |
| What ontology file asserts the element | cco:curated_in_ontology | exactly 1 URI reference to the ontology itself, ^^xsd:anyURI |

## Scope through Use Cases
The following sections give explicit scope for what design patterns are to be extended and need coverage. Use cases may be expressed with a visualization of a graph and an enumeration of classes, instances, relations, etc.

### General Account of Document Acts
Use cases
1. This person is responsible for the tree that fell on that house.
2. This person is designated an heir of that entire estate upon condition of the natural death of the estate's owner.
3. This person now has custody of that child who is a legal minor.
4. This priest pronounced that man and woman to be husband and wife. Later, a marriage license was signed by the parties to attest to it.
5. This person is the authority to waive her right to privacy.

Competency Questions
1. What are the permissions, prohibitions, and obligations represented in this document?
2. What special status was created by this document act, and what actions are obligated given that status?
3. What persons have special rights and privileges, in virtue of their vulnerable status?
4. What documents are authoritative to establish a person's claim to land ownership?
5. What travel restrictions hold for this parent and what role does the parent have in education decisions, given this joint-custody agreement?

### Commercial
Use cases
1. This bank hired an appraiser to assess the market value of that house.
2. Company1 made an offer for a contract to build house1, and the terms name a sub-contractor, company2, to install the plumbing and septic system in house1.
3. Customer1 purchased couch1 from business1, but the couch1 is not yet built.
4. This document is private. Yet organization1 is permitted to access (read) the section1 of the document, and organization2 is permitted to access (read) section1 and share its contents with third parties if relevant to advertising.
5. This customer has been banned from entering the building 
 
### Competency Questions
Com-CQ1. What contracts exist where this organization is a party?
Com-CQ2. What rights and obligations are enumerated in this service contract?
Com-CQ3. What processes performed by business1 are conditions that must be satisfied in order for business2 to have an obligation?
Com-CQ4. What rights does this employee have with respect to safe labor conditions?
Com-CQ5. What obligations does business1 have with respect to customer1?

### Biomedical Use Cases and Competency Questions
Bio-UC1. This specimen is stored in x repository. It is permitted for retreival (to any member of some organization).
Bio-UC2. This organization is a member of a network of organizations, and certain permissions hold for all members of the organization.
Bio-UC3. 

Bio-CQ1. What health organizations in a given state/province are not permitted to perform abortive surgical procedures?
Bio-CQ2. What What health organizations in a given state/province are not permitted to perform abortive surgical procedures?
Bio-CQ3. What surgical operations does this power of attorney document permit, and who holds the power of attorney?
Bio-CQ4. Who is the next of kin for this patient?
BIo-CQ5. 

### Government Use Cases and Competency Questions
- Gov-CQ1. What prohibitions are enumerated in this State law?
- Gov-CQ2. What citizens are eligible for this benefit according to the regulations in this welfare program? 
- Gov-CQ3. What regulations are in force at this location, given that it is within 3 overlapping jurisdictions?
- Gov-CQ4. What rights are recognized by this State's laws but not Federal law?
- Gov-CQ5. What laws come into effect in this jurisdiction when a majority of States ratify the law?

- Gov-UC1. This person has waived a right to sue that organization.
- Gov-UC2. Some government regulation requires all organizations of such-and-such type to anonymize all information about persons of such-and-such status.
- Gov-UC3. Document1 trumps document2. Document1 permits this type of action in jurisdiction1. Document2 prohibits this type of action in a larger jurisdiction2. Jurisdiction1 is located in jurisdiction2.
- Gov-UC4. Document2 trumps document1. Document1 permits this type of action in jurisdiction1. Document2 prohibits this type of action in a larger jurisdiction2. Jurisdiction1 is located in jurisdiction2.
- Gov-UC5. Regulation1 permits some person to perform some action, but regulation2 changes (is repealed or replaced?) and the permission no longer holds.


**Thesis: this set of use cases cannot be adequately captured without deontic roles.**
