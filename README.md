# UrWerk-Repo
The repository contains partial results of the Fraunhofer pilot project "**UrWerk**", the aim of which was to develop a framework for customised material data spaces that map the complex history of materials in the form of a network graph. 

![Data mapping and integration workflow applied in the use case 100Cr6 process history by combination of several software tools, connected by the scripts of GDTool](https://github.com/johannesrosenberger/UrWerk-Repo/blob/main/supplementary_material/data_mapping_and_integration_workflow.png?raw=true)

The EMMO domain ontology module Mechanical Testing, including our class definitions for both use cases, is published in the EMMO Repo at GitHub (https://github.com/emmo-repo/domain-mechanical-testing). Its current version 0.9.0 is based on EMMO version 1.0.0-alpha2.
In this repository an exemplary dataset of the use case 100Cr6 process history is published. It contains the data in triple form (based on class definitions of EMMO Mechanical testing) as RDF files as well as a graphical representation of the knowledge graph (ABox) as a .kdb file to be used with the software KnowledgeBaseBuilder (https://inforapid.org/webapp/login.php). The dataset in the subfolder “*data_knowledge_graph*” of the repository comprises:
- RDF files of an exemplary test series / material variant 100Cr6 [Straub21] one RDF file per specimen, ID 1420 - 1449, to be found in subfolder “Data-RDF”
- Excel spreadsheet with tabular data before RDF conversion “DataSpreadsheet.xlsx”
- Knowledge Graph of one specific 100Cr6 material variant [Straub21] to be used with software KnowledgeBaseBuilder, “KnowledgeGraph.kdb”
- Merged and inferred ontology for upload in graph database, either in turtle format “MergedAndInferredOntologyTurtle.ttl” or RDF-XML format “MergedAndInferredOntologyRDF-XML.xml”

[Straub21] *T. Straub, „Entwicklung einer validierten Methodik zur Berechnung der Schwing-festigkeit von Bauteilen aus höchstfesten Stählen, IGF-Vorhaben 19667 BG, Fraunhofer IWM, Universtität Weimar (MFPA),“ 2021.*

## Usage
The exemplary dataset can be uploaded to a graph database to explore our data structure and modeling approach using one exemplary test series. To enable this, the RDF files need to be uploaded to a graph database instance of your choice, here we used in our case AllegroGraph (https://allegrograph.com). The class definitions from the ontology module need to be uploaded separately. The original EMMO definitions can be used, but require a Reasoner software running within the graph database. A simpler solution is to perform the reasoning prior to uploading the ontology. This is why we provide also the merged and inferred ontology as turtle and RDF-XML files, which can be uploaded directly. All necessary modules from EMMO top level ontology are merged with the domain ontology modules and conveniently compiled in a single file. After upload, the data structure can be explored with the user interfaces of the graph database. An example of the “GRUFF” interface of AllegroGraph is shown below. 

![GUI in AllegroGraph for our dataset](https://github.com/johannesrosenberger/UrWerk-Repo/blob/main/supplementary_material/GUI%20interface%20in%20allegrograph.png?raw=true)

In addition, we provide exemplary SPARQL queries for filtering and reasoning in the folder “*code*”.

## Licenses
There are different licenses for each folder: 
- "*data_knowledge_graph*" and "*supplementary_material*" are published under **CC-BY-SA-4.0**.
- "*code*" is published under **MIT License**.

## Citation
*Sascha Fliegener, Johannes Rosenberger, Michael Luke, José Manuel Domínguez, Joana Francisco Morgado, Hans-Ulrich Kobialka, Torsten Kraft, Johannes Tlatlik*

*Digital methods for the lifetime assessment of engineering steels*

*Advanced Engineering Materials Volume... Issue...*

*Special Issue Digitalization in Materials Science and Engineering*

*2024*

*pages...*

*DOI...*

## Plattform Material Digital
![Logo_Material_Digital](https://raw.githubusercontent.com/johannesrosenberger/UrWerk-Repo/5ac81ea5eee91692d521fab6ad8ec5f9759e52dd/supplementary_material/Logo_MaterialDigital.svg)
https://www.materialdigital.de/
