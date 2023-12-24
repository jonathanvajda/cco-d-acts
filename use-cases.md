# CCO Document Acts Ontology Working Group (CODA WG)
This working group is to develop the theory and framework of Document Acts. Document Acts are processes which have 

## Use Cases, Competency Questions, and Intended Knowledge Graphs
Each use case is framed in terms of a type of scenario and/or a competency question. A scenario may be a set of assertions (information about entities and their relationships). A compentency question is an informal (or semi-formal) question for which some data would return as an answer. The competency question is used as a benchmark for whether the representation is sufficiently expressive to be able to return the information in view. A set of competency questions can be used as a set of requirements for a tell-and-ask system supported with an ontology. The questions can be formalized in terms of a SPARQL query. The use case or the competency question may be diagramed with the relationships, made explicit in a visualization of a graph of individuals, classes, and object and data properties asserted in the model. If the visualization represents knowledge, it may be considered an "intended knowledge graph."

Progress in providing coverage is tracked with the checklist below (or with an issue tracker link). Every use case is considered "covered" when:
- the representation exemplifies or extends the Common Core Ontologies' design pattern(s)
- the CCO-conformant design pattern is documented (in Word, PowerPoint, or otherwise)
- there is a sample of data in view (real or merely notional)
- there is a visualization that captures a graph of that sample data according to the design pattern (draw.io, PowerPoint, Visio, or otherwise). This is called an "intended knowledge graph."
- there is an OWL2 ontology file (owl, ttl, rdf) with opaque IRIs in a Documents Acts namespace, with all resources properly annotated
- a sample SPARQL query that formalizes the competency question is drafted

### Annotation Requirements
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
The following sections give explicit scope for what design patterns are to be extended and need coverage. Use cases may be exp

### General account Use Cases and Competency Questions
General-UC1. This person is an authority with respect to the use of this asset, but the person is not the owner.
General-UC2. This information is normally private (not for public). The first part of the document is permitted for organization 1 to access (read). The second part of the document is permitted for organization 1 and organization 2 to access (read).
General-UC3. Document1 trumps document2. Document1 permits this type of action in jurisdiction1. Document2 prohibits this type of action in a larger jurisdiction2. Jurisdiction1 is located in jurisdiction2.
General-UC4. Document2 trumps document1. Document1 permits this type of action in jurisdiction1. Document2 prohibits this type of action in a larger jurisdiction2. Jurisdiction1 is located in jurisdiction2.
General-UC5. Regulation1 permits some person to perform some action, but regulation2 changes (is repealed or replaced?) and the permission no longer holds.
General-UC6. 

General-CQ1. What authorities are recognized by law?
General-CQ2. What documents create obligations? (SELECT
General-CQ3. What organizations are prohibited from doing this action?
General-CQ4. 

### Biomedical Use Cases and Competency Questions

Bio-UC1. This specimen is stored in x repository. It is permitted for retreival (to any member of some organization).


Bio-CQ1. What health organizations in a given state/province are not permitted to perform abortive surgical procedures?
- [ ] Diagram(s) of an example intended knowledge graph
- [ ] Ontology resources asserted in an OWL2 file (owl, ttl, rdf)
- [ ] Documentation explaining reusable the design pattern

Bio-CQ2. What What health organizations in a given state/province are not permitted to perform abortive surgical procedures?

- [ ] Diagram(s) of an example intended knowledge graph
- [ ] Ontology resources asserted in an OWL2 file (owl, ttl, rdf)
- [ ] Documentation explaining reusable the design pattern

Bio-CQ3. What surgical operations does this power of attorney document permit, and who holds the power of attorney?

Next of kin

### 


**Thesis: this set of use cases cannot be adequately captured without deontic roles.**

T
