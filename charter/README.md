## Open Geospatial Consortium 

Submission Date: 2018-04-26

Approval Date: 2018-mm-dd

Publication Date: 2018-mm-dd

External identifier of this OGC® document:

Internal reference number of this OGC® document: **18-039**

Version: 1.0

Category: OGC® Interoperability Experiment

Editors: Rainer Häner, Sylvain Grellet

# OGC Project Document 18-039: Activity Plan for an OGC Interoperability Experiment

### Title: Borehole and associated data information Interoperability Experiment

### Abbreviation: The Borehole IE

## Summary

Borehole and associated data are crucial for many domains. They are used in any domain that need to probe the underground; geology (hydrogeology, oil and gas, mining), civil engineering (utilities, constructions, transportation) and environment (ice coring, limnology, etc.) A key element of boreholes is a spatial reference system that defines the trace of the borehole and the location of observations in 3D space. Examples are 2D reference systems or the horizontal component of 3D reference system combined with a dedicated height reference system, 3D reference systems, latitude/longitude combined with depth below surface, or even 'self-made' local reference systems. 3D depth information is complicated by the multiple methods used to describe the borehole trace, including absolute x/y/z values, periodic distance and inclination values, and more.

Even though several standards already exist to describe a borehole, its associated data and their position along a borehole (including OGC standards), they all restrict themselves to a specific viewpoint. Involving key implementers and editors of the existing standards, this Interoperability Experiment (IE) aims at clarifying the commonalities and differences of the diverse approaches by providing a semantic umbrella linked to the pre-existing work by distilling the core elements shared by all disciplines. This will provide the basis for establishing a better integration of existing standards and possibly a future common approach for describing boreholes.

The IE will produce the semantic umbrella and an OGC engineering report summarizing the achievements and listing the potential adjustments to be made on the pre-existing standards so that the system as a whole is at the end coherent. The IE will also test the consumption of the produced information files/flow, which will also be used as a demonstration artefact. Domain needs will stem from domain use cases where the proposed umbrella will be tested through crafted scenarios.

## Initiators

The OGC members who are initiators of this Interoperability Experiment are:

* BRGM
* Energistics
* Geoscience Australia
* Land Information New Zealand
* Natural Resources Canada
* Uppsala University, Sweden
* Helmholtz Centre Potsdam - GFZ German Research Centre for Geosciences

## Participants

The following OGC member organizations will participate in the IE

* BRGM
* Energistics
* Geoscience Australia
* Land Information New Zealand
* Natural Resources Canada
* Uppsala University, Sweden
* Helmholtz Centre Potsdam - GFZ German Research Centre for Geosciences
* State Geological Surveys of Germany via GFZ

## Description

The goal of the Borehole IE is to advance interoperability across domains using Borehole data. It will investigate the current models, identify common use cases, proposed a common umbrella model, and investigate the best use of GML linear referencing.

### Objectives

The objectives of the IE include:

* Do an inventory of relevant Borehole conceptual models and associated vocabularies.
* Document use cases related to borehole description and associated data.
* Explore how GML 3.3 (10-129r1, clause 9) Linear Reference can be used or improved.
* Proposed a common model/ontology that covers the use cases.
* Identify the differences between the proposed model and the existing solutions.

### Background

All human activities that need to investigate the underground are either relying on indirect observations methods like geophysics or direct observation by drilling a hole in the ground. While each domain has its own set of methods and interest (resource geologists look at rock properties relevant to mineral occurrences; hydrogeologists at water resources; civil engineers at mechanical properties; and the energy sector at fossil fuel potential) they all use the same basic engineering feature, a borehole.

Observations made by one discipline are usually highly relevant to the other disciplines. Therefore, it is essential to exchange information related to the spatial object ‘borehole’ in a consistent manner. Several standards are already available (e.g., logs, sample, continuous monitoring, etc.):

* OGC: GeoSciML (OGC 16-008[1]) and WaterML 2: Part 4 – GroundWaterML 2 (GWML2, OGC 16-032r2[2]),
* Industry: Energistics, RESQML, WITSML[3], PPDM [4], AGS Data Format for geotechnics [5], ...
* National: BoreholeML [6]
* Legal Obligation : Europe’s INSPIRE Geology theme data specification [7]

Each of these standards provide a domain oriented view that overlaps with the view of other domains on specific aspects:

* Boreholes are spatial reference objects, along which observations are made. In a sense, they are similar to a mapping Coordinate Reference System (CRS);
* Boreholes are associated with basic metadata regarding their creation (drilling methods, drillers, owners, etc.); and
* Boreholes have a set of construction artefacts (engineering objects) attached to them (casings, head works, etc.).

When it comes down to the exchange of borehole information in cross-silo, cross-domain, cross-legislation situations, a common view of essential borehole components is missing.

A domain-neutral solution for describing a borehole also exists (using OGC/ISO 19156 Observations and Measurements (O&M) along with other OGC SWE standards) but is not often fully implemented and too generic to cover detailed borehole information. Use of the O&M standard requires specialization along with specific constraints.

As such, GeoSciML Borehole is an extension of ISO 19156 that attempts to constrain the generic O&M model for boreholes. GroundWaterML 2 did the same exercise for water wells. But they both propose slightly different ways to link their respective domain features to the underground context.

Recent exchanges stemming from discussions within the OGC GeoScience Domain Working Group (DWG), IUGS / CGI GeoSciML SWG and the EU research infrastructure EPOS theme on Geological Information and Modelling [8] confirm such a need, the technical feasibility of the approach and, above all, the willingness of the community to engage in such exercise.

This IE seeks to gather parties that are implementing and/or involved in specifying and maintaining the above mentioned and other relevant standards

### Use Cases

The following use cases topics have been identified. They will be refined and complemented over the course of the IE.

* Scientific exchange within and across Research Infrastructures (EPOS, AuScope, etc.);
* Industrial (e.g., oil & gas or mineral resources);
* Cross Scientific-Industrial exchange between research and industry;
* Building and construction;
* Regulatory obligations such as EU INSPIRE directive [9] requiring all EU member states to provide Borehole information according to the data structure defined in its theme Geology. There will be a need to liaise with EU bodies (EC-JRC) to assess how the result of the IE could be proposed as a validated option within Europe.
* Geo-resources monitoring and exploitation such as groundwater, geothermal energy.

## Technical Approach

The IE will define semantics for borehole and associated data that meets the use cases’ information needs.

The IE will define a domain neutral / umbrella vocabulary for a general concept of borehole, which may eventually become its own specification and be properly reused by domains when needed.

Specific attention will be paid on the term ‘log’ often used to refer to two very different notions:

* ‘Logs’ that are the result of interpretation by a domain specialist where specific features, such as contacts, are recognized; and
* ‘Logs’ that are composed of regular (though not necessarily regularly spaced) observations of ‘fact’ – as in geophysics and imagery.

The formalism applied will consider the provision of an ontology and/or ISO 19100 XML/XSD model. It is not the purpose of this IE to define all the necessary missing registries of terms that are needed to describe all aspects of this topic.

The IE will also consider in its work best practices around linked data and semantic web technologies.

The IE will not seek to solve every controlled vocabulary issue encountered. The reuse and extension of pre-existing vocabularies and community defined Code Lists will be favored.

### Methodology

At the beginning of the IE, participants involved in the identified use cases will define the semantic requirements

By involving key implementers and editors of the identified standards, it will be possible to easily craft instance documents to test the semantic proposed. Successes, difficulties, and missing notions will be reported.

These results will be used to refine iteratively the semantic work and also to inform future work on standards and/or best practices especially via the IE engineering report.

### Demonstration Planning

The value added of the umbrella semantic will be tested through instance document set up and, hopefully, their consumption in generic clients.

### Component Development

The following components will be developed as part of the IE. Primary responsibility of each component as agreed by participants is included.

| Description | Implementers(s) |
| ----------- | --------------- |
| Use Case description | All |
| Borehole and associated data common model | All |
| Link with the identified standards (ex : GeoSciML4, GWML2, BoreholeML, Energistics, INSPIRE, etc. | All |
| Encode instance documents | All |
| Evaluate Documents | All |
| Engineering Report | All |


### Testing

The evaluation of the resulting model and testing documents will be done through inspection and analysis of required information to satisfy the use cases. Specific criteria defining what satisfaction means will be established early on in the IE.

## Deliverables

All deliverables for the project will be in the form of OGC engineering reports and static content hosted on a public OGC GitHub project.

### Documentation

An engineering report will summarize the overall IE and the group’s findings. The IE will be managed using GitHub issues, wiki, pages, and general code repository functionality. It is the intention of the IE initiators that all project artifacts will be made public through this repository upon IE conclusion.

## Schedule (TENTATIVE)

**Execution**

June 2018 - Use cases and semantic requirements,

Fall 2018 – First draft of the borehole semantic umbrella available. Tests and iterative enhancement

March TC 2019: First draft demonstration

June 2019: Demonstration and evaluation complete at summer TC

September 2019: IE complete, final document submitted

## Resource Plan

The IE will be co-lead by BRGM (Sylvain Grellet) and Helmholtz Centre Potsdam - GFZ (Rainer Haener).

The following resources will be available:

| | |
| ----------- | --------------- |
| Staffing | Each initiating and participating organization will provide adequate staff resources to support their defined responsibilities for the duration of the IE. |
| Hardware | Initiating organizations will provide hardware as needed to support the IE. Resources associated with the OGC GitHub organization are requested to house the IE’s work |
| Software | Initiating organizations will provide software as needed to support the IE. Resources associated with the OGC GitHub organization are requested to house the IE’s work. |
| Other Resources | Participants in the IE are self-funded. All expenses incurred in carrying out the IE will be assumed by the participating agencies within their regular line-of-business. |

[1] http://docs.opengeospatial.org/is/16-008/16-008.html

[2] http://docs.opengeospatial.org/is/16-032r2/16-032r2.html

[3] http://www.energistics.org/drilling-completions-interventions/witsml-standards/current-standards

[4] https://ppdm.org/ppdm/PPDM/Standards/PPDM/PPDM_Standards.aspx?hkey=fcd52d61-9bd5-4f27-9c91-a4b9fda3d2e8

[5] https://www.ags.org.uk/data-format/

[6] http://www.infogeo.de/home/boreholeML/

[7] http://inspire.ec.europa.eu/Themes/128/2892

[8] https://www.epos-ip.org/tcs/geological-information-and-modeling/data-services/wp15-services-and-architecture

[9] https://inspire.ec.europa.eu/inspire-legislation/26
