# CCO Document Acts Ontology Working Group (CODA WG)
This working group is to develop the theory and framework of Document Acts. Document Acts are processes which have ....

## Use Cases, Competency Questions, and Intended Knowledge Graphs
Each use case is framed in terms of a type of scenario and/or a competency question. A scenario may be a set of assertions (information about entities and their relationships). A competency question is an informal (or semi-formal) question for which some data would return as an answer. The competency question is used as a benchmark for whether the representation is sufficiently expressive to be able to return the information in view. A set of competency questions can be used as a set of requirements for a tell-and-ask system supported with an ontology. The questions can be formalized in terms of a SPARQL query. The use case or the competency question may be diagramed with the relationships, made explicit in a visualization of a graph of individuals, classes, and object and data properties asserted in the model. If the visualization represents knowledge, it may be considered an "intended knowledge graph."

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
2. This company made an offer for a contract to build a house, and the terms name that company as a sub-contractor to install the plumbing and septic system in the house.
3. This customer purchased a couch from that business, but the couch is not yet built.
4. This document is private. Yet this organization is permitted to access (read) the first section of the document, and that organization is permitted to access (read) the first section and share its contents with third parties if relevant to advertising.
5. This customer has been banned from entering any stores run by the same owner.
 
Competency Questions
1. What contracts exist where this organization is a party?
2. What rights and obligations are enumerated in this service contract?
3. What processes performed by business1 are conditions that must be satisfied in order for business2 to have an obligation?
4. What rights does this employee have with respect to safe labor conditions?
5. What obligations does this business have with respect to any customer?

### Biomedical
Use Cases
1. This insurance plan provides coverage for that tier 5 medication.
2. This organization is a member of a network of organizations, and certain permissions hold for all members of the organization with respect to sharing anonymized data.
3. This genome research organization has an obligation to report incidental findings to persons who have predispositions to life-threatening diseases and disorders.
4. This nation prohibits biological research that produces or uses embryonic stem cells.
5. This person receives a discount for this line of pharmaceutical products and preference on that organ transplant waitlist.

Competency Questions
1. Who has rights as next-of-kin for this patient's remains?
2. What health organizations in a given state/province are not permitted to perform abortive surgical procedures?
3. What surgical operations does this power of attorney document permit, and who holds the power of attorney?
4. Given this malpractice claim against this health provider, what obligations does the health provider have with respect to informing their patients?
5. What healthcare options are available to this 14 year old patient, without a parent's consent?

### Government
Use Cases
1. What prohibitions are enumerated in this State law?
2. What citizens are eligible for this benefit according to the regulations in this welfare program? 
3. What regulations are in force at this location, given that it is within 3 overlapping jurisdictions?
4. What rights are recognized by this State's laws but not Federal law?
5. What laws come into effect in this jurisdiction when a majority of States ratify the law?

Competency Questions
1. This person has waived a right to sue that organization.
2. Some government regulation requires all organizations of such-and-such type to anonymize all information about persons of such-and-such status.
3. Document1 trumps document2. Document1 permits this type of action in jurisdiction1. Document2 prohibits this type of action in a larger jurisdiction2. Jurisdiction1 is located in jurisdiction2.
4. Document2 trumps document1. Document1 permits this type of action in jurisdiction1. Document2 prohibits this type of action in a larger jurisdiction2. Jurisdiction1 is located in jurisdiction2.
5. Regulation1 permits some person to perform some action, but regulation2 changes (is repealed or replaced?) and the permission no longer holds.

**Thesis: this set of use cases cannot be adequately captured without deontic roles.**
