## An Ontology for Document Acts that Extends the Common Core Ontologies (CCO)
CCO-D-Acts fills a gap in representation of social, legal, normative, and deontic entities for ontologies that rely on the Common Core Ontologies (CCO) suite. Within the Basic Formal Ontology (BFO) ecosystem the Document Acts (D-Acts) ontology is an extension of the Information Artifact Ontology (IAO) that represents the generic domain of entities relevant to the creation, modification, or termination of social arrangements by means of some document. Examples of such documents include marriage licenses, mortgage contracts, parking tickets, etc. The Informed Consent Ontology (ICO) imports D-Acts, for example.

### Project Parts
- OWL2 file, serialized in Turtle (TTL)
- Documentation on how to import
- Documentation on alignment decisions

### Purpose
The Common Core Ontologies (CCO) are a suite of mid-level ontologies conformant with BFO, that provide representation of generic domains such as agents, artifacts, events, information, etc. The Information Entity Ontology (IEO) is one of those mid-level ontologies of the CCO suite, with a high overlap in domain as IAO. However, IAO and IEO have conflicting models. There should only be one representation of information entities: the Information Artifact Ontology (IAO). But the Information Entity Ontology (IEO) is more accurate and rigorous in some aspects. Since D-Acts is an extension of IAO, it would benefit those who rely on CCO ontologies to have a D-Acts counterpart conformant with IEO. This project proposes that counterpart: **CCO-D-Acts**. Where all of this development would be, ideally, is that IAO updates to IEO's design patterns, and as the Document Acts Ontology (D-Acts) would need to change, the development here (CCO-D-Acts) would speed up that process. This project should assist with that transition while reducing downtime.

### Principles
Basic Formal Ontology adopts realism, fallibilism, and adequatism ([Otte, Beverley and Ruttenberg, 2021](https://philarchive.org/archive/OTTBBF)). _Realism_ in this context is the view that we can know and assert instances (individuals) and types (universals) that are real, beyond merely how we think or represent things. _Fallibilism_ is the view that our assertions about the real world can be mistaken, if we represent the world contrary to the way the world is (our assertions and models can fail to correspond to the real world). _Adequatism_ is the view that the entities in view need not be reduced or explained away as illusory or unnecessary in terms of more fundamental entities, but rather are suitable and properly said at the level of granularity and scope for the domain. This also means that there can be multiple representations of how the world is without contradiction. Some representations conflict, but differences do not entail contradiction, since the differences may be merely in scope, aspect, form, or granularity. That said, in the ideal world, all ontologies would follow the same design patterns and there would be no overlap in domains in the same perspective (asserting the same entities).

## Development
- Join our National Center for Ontology Research Working Group for Documents Acts: [NCor D-Acts WG](https://johnbeve.github.io/NCOR-Test/d-acts-wg/)
- Current efforts in Use case coverage can be found in the [Use Case Markdown](https://github.com/jonathanvajda/cco-d-acts/blob/main/use-cases.md) in this repository
- Design pattern slide deck. See: [Google Slides Design Patterns](https://docs.google.com/presentation/d/16hYjzlTm1N38zenNGiNq2YENGAhrtqd6zDJ8mdf3g70/edit#slide=id.g2db1d96c9a8_0_0)
- Running list of terms, staging the lexicon before the ontology file (term list, definitions, axioms to be added, sources identified, etc.). See: [Google Sheets Lexicon](https://docs.google.com/spreadsheets/d/1tC-z5rIos7nOuSaQSgVJ5ik4RHgvnObt/edit#gid=177562300)
- Open issues: see [issue tracker](https://github.com/jonathanvajda/cco-d-acts/issues) for problems 

## Resources
- The original [Document Acts Ontology (D-Acts)](https://github.com/d-acts/d-acts)
  - Mathias Brochhausen, et al.
- Common Core Ontologies (CCO) suite [GitHub repository](https://github.com/CommonCoreOntology/CommonCoreOntologies)
  - CUBRC et al.
- "Common Core Conformant Definitions for an Ontology of Commercial Exchange" ([Eric C. Merrell, Olivier Massin & Barry Smith](https://philarchive.org/rec/MERCCC)

## Licensing
https://creativecommons.org/licenses/by/4.0/
