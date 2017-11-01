## {{site.data.fhir.igName}} Implementation Guide
{:.no_toc}

{% include pub-publish-box.html %}


<!-- TOC  the css styling for this is \pages\assets\css\project.css under 'markdown-toc'-->

* Do not remove this line (it will not be displayed)
{:toc}


<!-- end TOC -->

## Introduction

The US Core Implementation Guide is based on [FHIR Version {{site.data.fhir.version}}]({{site.data.fhir.path}}) and defines the minimum conformance requirements for accessing patient data as defined by the [Argonaut] pilot implementations and the [ONC 2015 Edition Common Clinical Data Set (CCDS)]. These profiles are intended to be the foundation for future US Realm FHIR implementation guides. In addition to Argonaut, they are used by [DAF-Research], [QI-Core], and [CIMI].  Under the guidance of HL7 and the HL7 US Realm Steering Committee, the content will expand in future versions to meet the needs specific to the US Realm.

These requirements were originally developed, balloted, and published in FHIR DSTU2 as part of the [Office of the National Coordinator for Health Information Technology (ONC)] sponsored [Data Access Framework] (DAF) project. For more information on how DAF became US Core see the [US Core change notes](uscore-change-notes.html).  

## US Core Actors

The following actors are part of the US Core IG:

* US Core Requestor: An application that initiates a data access request to retrieve patient data. This can be thought of as the client in a client-server interaction.
* US Core Responder: A product that responds to the data access request providing patient data. This can be thought of as the server in a client-server interaction.


## US Core Profiles

The list of US Core Profiles is shown below.  Each profile defines the minimum mandatory elements, extensions and terminology requirements that **MUST** be present. For each profile requirements and guidance are given in a simple narrative summary. A formal hierarchical table that presents a [logical view] of the content in both a differential and snapshot view is also provided along with references to appropriate terminologies and examples.  In addition each profile has a "Quick Start" section which is intended as an implementer friendly overview of the required search and read operations.

{% include list-ballot-profiles.xhtml %}
US Core adopts the [Vitals Signs Profile](us-core-vitalsigns.html) from FHIR Core.

*Note on Searches based on a date or date range:*

- Allergies, Immunizations, Medications, Problems and Health Concerns, UDI, Smoking Status do not require a date range search since a system should return all relevant resources.
- Vital Signs, Laboratory Results, Goals, Procedures, and Assessment and Plan of Treatment include date range search requirements in the Quick Start section on the profile page.

See [2015 Edition Common Clinical Data Set] for a mapping to the CCDS.

## US Core Conformance Requirements

The [Capability Statements Section](capstmnts.html) outlines conformance requirements for the US Core Servers and Client applications, identifying the specific profiles that need to be supported, the specific RESTful operations that need to be supported, and the search parameters that need to be supported. Note: The individual US Core profiles identify the structural constraints, terminology bindings and invariants, however, implementers must refer to the conformance requirements for details on the RESTful operations, specific profiles and the search parameters applicable to each of the US Core actors.

----


Primary Authors: Brett Marquard, Nagesh Bashyam, Eric Haas

Secondary Authors: Grahame Grieve, Lloyd McKenzie



[QI-Core]:https://oncprojectracking.healthit.gov/wiki/display/TechLabSC/CQF+Home
[CIMI]:http://www.opencimi.org
[Argonaut]: http://argonautwiki.hl7.org/index.php?title=Main_Page
[DAF-Research]: http://hl7.org/fhir/us/daf-research/index.html
[US Core Security]: US Core-security.html
[Office of the National Coordinator for Health Information Technology (ONC)]: http://www.healthit.gov/newsroom/about-onc
[Data Access Framework]: http://wiki.siframework.org/Data+Access+Framework+Homepage
[Argonaut]: http://argonautwiki.hl7.org/index.php?title=Main_Page
[ONC 2015 Edition Common Clinical Data Set (CCDS)]: https://www.healthit.gov/sites/default/files/2015Ed_CCG_CCDS.pdf
[profiles]: {{site.data.fhir.path}}/profiling.html
[logical view]: {{site.data.fhir.path}}/formats.html#table
[StructureDefinitions]: {{site.data.fhir.path}}/structuredefinition.html
[Value sets]: {{site.data.fhir.path}}/valueset.html
[CodeSystem]: {{site.data.fhir.path}}/codesystem.html
[ConceptMap]: {{site.data.fhir.path}}/conceptmap.html
[NamingSystem]: {{site.data.fhir.path}}/namingsystem.html
[FHIR Conformance Rules]: {{site.data.fhir.path}}/CapabilityStatement-rules.html
[dataAbsentReason]: {{site.data.fhir.path}}/extension-data-absent-reason.html
[FHIR Terminology]: {{site.data.fhir.path}}/terminologies.html
[FHIR RESTful API]: {{site.data.fhir.path}}/http.html
[HTTP]: {{site.data.fhir.path}}/http.html
[FHIR Data Types]: {{site.data.fhir.path}}/datatypes.html
[FHIR Search]: {{site.data.fhir.path}}/search.html
[FHIR Resource]: {{site.data.fhir.path}}/formats.html
[2015 Edition Common Clinical Data Set]: guidance.html#edition-common-clinical-data-set
