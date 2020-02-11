# Lesson 4.3 Introduction to Data Interoperability

## Learning outcomes

At the end of this lesson, learners will \(be able to\):

* Understand the basics of data interoperability
* Identify the different types and layers of interoperability
* Understand the basics of semantic interoperability
* Choose the vocabularies that better fit their needs

## 1.   Introduction

Data interoperability is the ability of a data set to be reused by any system without special effort.

There are different layers to data interoperability: data can be technically interoperable thanks to a machine-readable format \(e.g. CSV\) and an easy-to-parse structure \(e.g. JSON\), but in order for an external system to perform more operations on a dataset, the “meaning” of data in the structure has to be explicit, and this is achieved through semantic interoperability, by using metadata and values that have been previously assigned an unambiguous meaning and an identifier that can be used across systems.

This lesson introduces the different layers of data interoperability: “foundational” or infrastructural \(exposure protocols\), structural \(file formats and content structure\) and semantic \(use of metadata and values from agreed vocabularies\). It only provides an overview and some examples: mastering the technologies for data interoperability would require a dedicated course and is something that is expected only of developers and data engineers.

However, a good understanding of the possible technological choices is useful both for data reusers, who should be able to assess the level of interoperability of the data they want to reuse, and for agricultural data/service providers who want to make sure their data is interoperable with other systems.

A longer section is devoted to semantic interoperability, as it is the most sector-specific aspect of data interoperability: while protocols and formats/structures are sector-agnostic, semantics are created and agreed upon in specific domains and in the case of agricultural data it is very important to know which semantic structures have been published in the domain and for which sub-domains \(agronomy, food and nutrition, natural resources…\) or types of data \(soil data, weather data, crop growth data…\).

The next lesson will focus on examples of interoperable data using vocabularies created for farm data.

## 2.   Data interoperability

The most used definition of ‘interoperability’ on the web is: ‘the ability of a system or a product to work with other systems or products without special effort on the part of the user’. Wikipedia defines it as ‘a characteristic of a product or system, whose interfaces are completely understood, to work with other products or systems, at present or future, in either implementation or access, without any restrictions’.

When it comes to data interoperability, considering that data are serialised in datasets, the definitions above can be applied easily to a dataset as a product.

In the [proceedings of a conference](http://www.fao.org/docs/eims/upload/297074/IECProceedings-main-doc.pdf) organised by the CIARD community on data interoperability for agriculture, data interoperability was defined as ‘**a feature of datasets … whereby data can be easily retrieved, processed, re-used, and re-packaged \(“operated”\) by other systems**.’

There are some definitions that define it as the interoperability ‘between two systems’, however it is a common view that something is really interoperable \(or more interoperable\) when as many systems as possible can interoperate it. Even more, by using certain data formats and applying certain data standards, data can be made ‘interoperable by design’ without necessarily knowing with which system they will be interoperable: planned interoperability with specific systems means that the data will be ‘tightly coupled’ with those systems, while maximised interoperability aims at loose coupling with as many systems as possible.

However, there will never be something like universal or perfect interoperability, a way of exposing data that will be suitable for all possible cases. Interoperability is always relative to a system of shared standards and common ways of using data that are in some cases very broad and all-purpose \(like Dublin Core or [schema.org](https://schema.org/) and a generic search engine use case\) and in other cases very specific to scientific or interest communities \(like data specifications and visualisations of gene sequences\).

Indeed, the definitions above define interoperability as a feature of data\(sets\) alone, which is correct because they are the object of the interoperation, but the ecosystem of actors and products that have to co-operate for achieving full interoperability is broader: an interesting definition of interoperability that highlights the importance of ‘shared expectations’ is the one from the Data Interoperability Standards Consortium \(DISC\): ‘[Data interoperability](http://datainteroperability.org/) addresses the ability of systems and services that create, exchange and consume data to have clear, shared expectations for the contents, context and meaning of that data.’

### 2.1. Levels of interoperability

Interoperability can be achieved at different levels. While Wikipedia distinguishes between syntactic interoperability and semantic interoperability, a more granular distinction is made in the classification of types of interoperability by the [Healthcare Information and Management Systems Society](http://www.himss.org/library/interoperability-standards/what-is-interoperability) \(HIMSS\):

‘**Foundational**’ interoperability allows data exchange from one information technology system to be received by another and does not require the ability for the receiving information technology system to interpret the data.

This level is about infrastructural interoperability and mostly about transmission protocols, which will not be addressed here as it is not of interest to the data manager, but it also covers some higher-level exchange protocols, mostly working on top of the common HTTP protocol \(for instance special REST APIs like OAI-PMH, SPARQL, Linked Data API or content negotiation based on HTTP content-type requests\). These may be of interest to data managers because, before being read and understood, data has to be transmitted, and there are different and more convenient ways to do this besides FTP downloads.

‘**Structural**’ interoperability is an intermediate level that defines the structure or format of data exchange \(i.e., the message format standards\). Structural interoperability defines the syntax of the data exchange. It ensures that data exchanges between information technology systems can be interpreted at the data field level.

This is the level where file formats and data formats play the most important role and it is the level where \(meta\)data become ‘machine-readable’ and can be parsed by machines: the easier it is for machine to parse the \(meta\)data format/syntax \(XML, Json, CSV…\) the more structurally interoperable data are.

‘**Semantic**’ interoperability provides interoperability at the highest level, which is the ability of two or more systems or elements to exchange information and to use the information that has been exchanged. Semantic interoperability takes advantage of both the structuring of the data exchange and the codification of the data including vocabulary so that the receiving information technology systems can interpret the data.

While with structural interoperability machines understand what the different elements are \(and their reciprocal structural relation\), with semantic interoperability they also understand the meaning of those elements and can process them with semantics-aware tools and do some advanced reasoning. Data formats are not enough for this: semantic technologies allow to embed machine-readable semantic elements from agreed vocabularies in \(meta\)data serialised in most of the existing data formats, although the most suitable formats for this so far are the various flavours of RDF \(RDF/XML, Turtle, N-Triples\) and JSON-LD.

For more detailed recommendations on how to implement data interoperability, the W3C ‘[Data on the Web Best Practices](https://www.w3.org/TR/dwbp/) is probably the best reference document. It is heavily based on the ‘Linked Data’ approach, but many of the recommendations help implement interoperability at different levels, even if not aiming at 100% linked data.

### 2.2. Interoperability of data and metadata

Data without metadata cannot be understood by machines. Data normally come with metadata.

The definition of data in Wikipedia is: ‘**Data are** **values of qualitative or quantitative variables, belonging to a set of items**.’ As such, in the end data are always part of a collection \(a set of items\) and in the individual item \(row, record\) in the set, data are the values of some variables, so they will always be encapsulated in some form of key-value pair where the key \(the variable\) is in the end a metadata element that gives meaning to the data. This key-value pair is what in [FAIR](https://www.force11.org/fairprinciples) terms is called ‘a single association between two concepts’, which is ‘one of the smallest possible 'Data Elements’.

Both parts in the key-value pair can present issues of interoperability, so one can deal with issues of interoperability of the metadata \(e.g. agreed schemas for metadata elements, agreed variable names\) and issues of interoperability of the data/value \(e.g. agreed controlled lists/ranges from which the value has to be taken, or syntax issues\). However, since it is also common to consider controlled values and specification of syntax or unit of measure as ‘metadata’ \(especially because they should be ideally defined by separate metadata elements and not within the value itself\), one can also say that interoperability is mostly about metadata. The interoperability of data is achieved through the interoperability of metadata: for instance, one wants the metadata ‘air temperature’ to be interoperable to then get the actual value \(the data\) that one needs – the number that expresses the value will never be findable or understandable per se without the associated metadata.

This lesson will follow the same convention adopted in the FAIR guiding principles mentioned above, using the term \(meta\)data when something applies indifferently to data and metadata.

## 3.   Infrastructural interoperability: exchange protocols

The most popular protocols for exposing data as a service are the Open Archives Initiative Protocol for Metadata Harvesting \(OAI-PMH\) and SPARQL. OAI-PMH and SPARQL are technically RESTful\[1\] APIs and like all APIs they expose ‘methods’ which accept a number of parameters and these methods can be called via an HTTP request and return a machine-readable response.

Besides OAI-PMH and SPARQL, it is very common to have data exposed through custom APIs, with standardized documentation about parameters, data types and return values.

**OAI-PMH** was born in the library environment and it was conceived mainly for metadata, but it can be used to expose any type of ‘records’.

The methods of the OAI-PMH API are designed to enable a series of calls that allow the caller \(an application\) to preliminarily check some metadata about the repository \(the name, what metadata schemas are supported, which subsets can be retrieved…\) and then retrieve records filtered according to metadata format, date ranges, subsets. Records can be retrieved in smaller batches using a ‘resumption token’.

\*\*\*\*[**SPARQL**](https://en.wikipedia.org/wiki/SPARQL) is a language for querying RDF data, but it is also the name of the protocol that enables the query to be sent via an HTTP request and get the response in several RDF-enabled formats \(RDF/XML, Turtle, JSON…\).

Compared to OAI-PMH, SPARQL allows for much more complex queries built using the powerful RDF triple grammar and can expose triples with any type of subject \(a dataset, an organisation, a place, a topic…\) all from the same interface. This makes it possible to filter data very granularly and look up other properties \(e.g. labels\) of resources referenced by URIs. SPARQL clients can also send the same query to several SPARQL engines and combine the responses: the use of URIs allows the client to merge duplicates and consolidate properties for the same entity coming from different systems.

Other protocols have been developed in scientific communities, building on common scientific data exchange practices, focusing on efficiency of data transfer \(catering for large amounts of data\) and leveraging traditional exchange formats like NetCDF and HDF5 \(see next section\). An example is OPeNDAP.

**OPeNDAP** \(‘[Open-source Project for a Network Data Access Protocol](https://en.wikipedia.org/wiki/OPeNDAP)’\) is ‘a data transport architecture and protocol widely used by earth scientists. The protocol is based on HTTP and \[…\] includes standards for encapsulating structured data, annotating the data with attributes and adding semantics that describe the data. \[…\] An OPeNDAP client sends requests to an OPeNDAP server and receives various types of documents or binary data as a response. \[…\] Data on the server is often in HDF or NetCDF format, but can be in any format including a user-defined format. Compared to ordinary file transfer protocols \(e.g. FTP\), a major advantage using OPeNDAP is the ability to retrieve subsets of files, and also the ability to aggregate data from several files in one transfer operation.’

The choice of protocols to implement to share one’s data should be definitely influenced primarily by the community with which data are expected to be shared and then by technical considerations such as ease of implementation, support for specific formats and general support for the data sharing principles.

For example, OPeNDAP is widely used by governmental agencies such as NASA and NOAA to serve satellite, weather and other observed earth science data, so it could be a good choice for institutions sharing these or similar types of data. On the other hand, if wider sharing across communities is desired, a custom API or known APIs like OAI-PMH or SPARQL can be preferred.

## 4.   Structural interoperability: formats and structures

This is the level where \(meta\)data become machine-readable. However, ‘machine-readable’ in its most literal sense is not enough for structural interoperability: in order for machines to understand the structure of the \(meta\)data, i.e. which are the labels/metadata elements/column names/variables and which are the values, and whether there’s a hierarchy, the \(meta\)data have to be structured enough for a machine to extract individual values.

In other words, \(meta\)data have to be not just readable but ‘parsable’ by machines. Since ‘parsing’ means ‘splitting a file or other input into pieces of data that can be easily stored or manipulated’, the more regular and rigorous a format is, the easier it is to parse it. Ideally, parsable formats have a published specification so that developers know how the structure is built and can write parsers accordingly. So, this level of interoperability is achieved through the choice of the most ease to parse data format.

There are many file formats that are parsable by machines. What makes a file format more easily parsable and therefore more interoperable is:

* The simplicity of the structure: the fewer the elements of the structure and the fewer the possible constructs are, the easier it is for a machine to parse the file without too complex reasoning. On the other hand, the format should also cater for complex data structures: the most suitable file format is the one that combines simplicity with enough flexibility to represent complex data structures.
* The rigorousness and ‘regularity’ of the structure: the fewer the options to serialise the same thing in a different way, the easier it is for a machine to parse the file and identify the role of each element.
* The existence of a clear and open specification for the format, which makes it easy for any developer to write parsers. \(Many formats are tied to a software product and can be correctly and fully parsed only by that product. This makes their interoperability level very low.\)
* An additional help is the existence of software libraries and APIs that can parse the format.

The formats that are considered the most interoperable against the criteria above are CSV, XML and JSON.

Binary array-based formats like [NetCDF](http://www.unidata.ucar.edu/software/netcdf/docs/) and [HDF5](https://support.hdfgroup.org/HDF5/doc/H5.format.html) retain a special place for their use by researchers. They will not be described here for a few reasons: they are more tied to specific software libraries \(however many tools can read them\); they are still more oriented towards compactness and efficiency of data transmission than towards broader interoperability, especially semantic interoperability; and some work has already been done to represent NetCDF in CSV \(the CEDA [BADC-CSV](http://help.ceda.ac.uk/article/105-badc-csv) format\) and in XML \(the [UNIDATA NcML](http://www.unidata.ucar.edu/software/thredds/current/netcdf-java/ncml/#NcML22)\).

**CSV \(comma-separated values\)** files have a simple tabular format with a header record with column names, commas to mark the field boundaries and line feeds to mark the record boundaries.

[CSV](https://www.w3.org/TR/tabular-data-primer/) is the simplest data format and very much used for typical tabular data like statistics or observations, but it cannot represent complex structures and is not documented in a machine-readable way: ‘There is no mechanism within CSV to indicate the type of data in a particular column, or whether values in a particular column must be unique. It is therefore hard to validate and prone to errors such as missing values or differing data types within a column.’\[13\] Some work to improve the interoperability of CSV files has been done by the W3C Working Group on ‘[CSV on the Web: Use Cases and Requirements](https://www.w3.org/TR/csvw-ucr/)’.

**XML \(**[eXtensible Markup Language](https://en.wikipedia.org/wiki/XML)\) is ‘a markup language that defines a set of rules for encoding documents in a format that is both human-readable and machine-readable. The design goals of XML emphasise simplicity, generality, and usability across the Internet.’ \(see Figure 1\).

The most interesting aspect of XML in terms of interoperability is the support of the definition of ‘schemas’ to which a specific XML document can declare to conform. Schemas are machine-readable documents that specify how to name and organise the elements in an XML document and can define hierarchies, constraints etc.

Dataset metadata in XML can reach a high level of complexity.

![Figure 1 Example of a generic XML structure for a dataset](../.gitbook/assets/image%20%2842%29.png)

**JSON \(**[JavaScript Object Notation](https://en.wikipedia.org/wiki/JSON)**\)** is ‘an open-standard file format that uses human-readable text to transmit data objects consisting of attribute–value pairs and array data types \(or any other serialisable value\)’.

JSON has a good combination of simplicity and flexibility in terms of data structures \(it was born as a format to represent programming data objects of any kind\) and it now has support for the definition of [schemas ](http://JSON-schema.org/)for validation purposes. Given the ease of use of JSON structures in programming languages, JSON is the serialisation format preferred by programmers.

![Figure 2 Example of JSON structure](../.gitbook/assets/image%20%2829%29.png)

Of the three, XML is traditionally the one considered as the best combination of \(a\) simplicity; \(b\) flexibility for complex data structures; and \(c\) support of schema definitions that set constraints and help validation and parsing. However, considering that JSON also supports schemas and that both XML and JSON can represent RDF \(see below\), JSON can be considered as suitable as XML.

Other formats that are extremely well interoperable are the main native RDF formats, Turtle and N-Triples.

**RDF**. The [Resource Description Framework](https://en.wikipedia.org/wiki/Resource_Description_Framework) \(RDF\) is ‘a general method for **conceptual description or modeling of information**’. As such, it is not a format and not tied to a specific format: any format that can represent the basic RDF ‘grammar’ \(“triples”\) can implement RDF.

The RDF grammar is based on statements made of **subject – predicate – object**; each statement is a ‘triple’ and the assumption is that combinations of such triples can represent and describe everything. Ideally all three components of the statement should be represented by Unique Resource Identifiers \(URIs\) that always refer univocally to the same entity.

The triples syntax is very simple:

```text
Subject (node) - Predicate / property (arc) -  Object (node)
<book_war&peace_URI> – <has­_title> – ‘War and Peace’
<book_war&peace_URI> – <is_of_type> – <book_type_URI>
<book_war&peace_URI> – <has_author> – <tolstoj_URI>
<tolstoj_URI> – <is_of_type> – <person_type_URI>
<tolstoj_URI> – <has_name> – ‘Lev Tolstoj’
```

Using URIs also for the predicates makes it possible to look up the meaning of the property in a published “vocabulary” \(see next section on semantic interoperability\).

The RDF grammar has been successfully applied to: \(a\) XML: XML/RDF is not really a new “format” \(it’s still formally XML\), but rather an XML that uses specific constraints that enforce the triple logic; and \(b\) JSON: the JSON-LD \([JSON for Linking Data](https://json-ld.org/)\) specification provides a method of encoding Linked Data as JSON.

## 5.   Semantic interoperability: vocabularies

All the data formats seen in the previous lesson define only data structures, how to encode fields/variables and values, and the only thing a machine can do is parse the structure and extract variables and values, without knowing how to treat each of them. Variables and values have a meaning which in many cases can be only understood by humans \(and in some cases only by humans who speak the same language and know the conventions of the same discipline\).

Human beings can interpret data through human-readable semantics that have always been used in \(meta\)data in different ways: a string to identify the topic of something or the colour of a thing \(e.g. in germplasm phenotypical descriptions\), codes taken from a code list of authoritative values \(e.g. type of soil\) or conventional variable names. But as already mentioned, interoperability is all about being understood by computer software: strings can be different in each dataset and in different languages, and even codes without a reference system behind them do not mean anything to computers and do not allow them to make decisions on how to treat the values.

If on the other hand the metadata contained information on the reference system \(a ‘semantic structure’ like a thesaurus or a code list\) from which each variable and each value came, and that semantic structure were machine-readable and provided some stable identifiers that computer programs could use as stable values to design their behaviour \(e.g. using the values as common search values across different datasets\), one would have achieved semantic interoperability.

So, on the one hand the metadata have to embed information on the reference semantic structures and point to the exact elements they are using from that structure; on the other hand these semantic structures, like the data, have to be ‘serialised’ in such a way that machines can read and process them, and use them to interpret the data.

Details on how to publish a semantic structure, or a ‘vocabulary’, in machine-readable format are beyond the scope of this lesson. In short, for our purposes in this lesson, let us say that such vocabularies are published as datasets, whose records are terms/concepts and their related descriptions, codes and ideally URIs, in a machine-readable format – for the moment let us assume XML or RDF/XML.

### 5.1. Semantic structures or ‘vocabularies’

Vocabularies are agreed sets of terms, possibly with defined relationships between them. This includes both terms used for description metadata, like metadata element names, properties, predicates \(so terms in **description vocabularies**: metadata schemas, ontologies…\) and terms used to categorise, annotate, classify \(so terms in **value vocabularies**: thesauri, code lists, classifications, authority lists…, also sometimes called ‘Knowledge Organisation Systems’ \(KOS\)\).

There is no formal classification of types of vocabularies \(which in itself could be a useful example of a value vocabulary\).

Limited to what was defined above as “value vocabularies”, the exercise of creating a taxonomy of vocabulary types has been partially done by the [Dublin Core](http://wiki.dublincore.org/index.php/NKOS_Vocabularies#KOS_Types_Vocabulary) initiative: their ‘KOS Types Vocabulary’ is quite useful to give an idea of the great variety of KOS and of the mixture of features that are combined in their definition:

* **categorisation scheme**: loosely formed grouping scheme
* **classification scheme**: schedule of concepts and pre-coordinated combinations of concepts, arranged by classification
* **dictionary**: reference source containing words usually alphabetically arranged along with information about their forms, pronunciations, functions, etymologies, meanings, and syntactical and idiomatic uses
* **gazetteer**: geospatial dictionary of named and typed places
* **glossary**: collection of textual glosses or of specialised terms with their meanings
* **list**: a limited set of terms arranged as a simple alphabetical list or in some other logically evident way; containing no relationships of any kind
* **name authority list** or authority file: controlled vocabulary for use in naming particular entities consistently
* **ontology**: formal model that allows knowledge to be represented for a specific domain; an ontology describes the types of things that exist \(classes\), the relationships between them \(properties\) and the logical ways those classes and properties can be used together \(axioms\) \[see below a note on how an ontology can be seen as a KOS but also as a description vocabulary, an extended schema\]
* **semantic network**: set of terms representing concepts, modeled as the nodes in a network of variable relationship types
* **subject heading scheme**:  structured vocabulary comprising terms available for subject indexing, plus rules for combining them into pre-coordinated strings of terms where necessary
* **synonym ring**: set of synonymous or almost synonymous terms, any of which can be used to refer to a particular concept
* **taxonomy**: scheme of categories and subcategories that can be used to sort and otherwise organise items of knowledge or information
* **terminology**: set of designations belonging to one special language
* **thesaurus**: controlled and structured vocabulary in which concepts are represented by terms, organised so that relationships between concepts are made explicit, and preferred terms are accompanied by lead-in entries for synonyms or quasi-synonyms.

As for description/modelling vocabularies, there is no authoritative list of, but the most commonly used such types are:

* **schema** \(or metadata element set\): any set of metadata elements, like XML schemas, RDF schemas or less formalised set of descriptors
* **application profile**: a schema which consist of metadata elements drawn from one or more namespaces, combined together by implementors, and optimised for a particular local application
* **messaging standard**: standards which describe how to format syntactically \(and sometimes semantically\) a message usually describing some event- or time-related information; messages are triggered by an event and transmitted in some way
* **ontology**, which can define complex schemas with constraints and rules for reasoning.     

As can be seen from the two lists above, ontologies are a special case: ‘In computer science and information science, an [**ontology**](https://en.wikipedia.org/wiki/Ontology_%28information_science%29) is a formal naming and definition of the types, properties, and interrelationships of the entities that really or fundamentally exist for a particular domain of discourse.’ As such, it can be used for multiple purposes: it can be used as a description vocabulary, using the relations or even the classes defined by the ontology as metadata elements/properties describing your data \(e.g. ‘extreme temperature resistance’ or ‘frost resistance’ in the [Wheat Trait Ontology](http://vest.agrisemantics.org/content/wheat-trait-ontology)\), or as a value vocabulary, using classes or entities as terms for controlled values \(e.g. wheat illnesses like Puccinia striiformis from the Wheat Trait Ontology, or countries from the [FAO Geopolitical Ontology](http://vest.agrisemantics.org/content/geopolitical-ontology)\).

Sometimes the boundaries between a schema and an ontology are blurred, but perhaps what can be considered typical of an ontology is the ‘functional’ more than descriptive design: classes, properties and especially relationships are designed as a model that is ‘actionable’ and can be used by applications for reasoning. However, the tendency nowadays is to use just the word ‘vocabulary’ and not delve too much into the definition of the different types. See the [W3C page](https://www.w3.org/standards/semanticweb/ontology) on ontologies. 

Examples of metadata vocabularies are:

* [Dublin Core](https://www.dublincore.org/specifications/dublin-core/dces/), a metadata set providing metadata elements to describe almost any resource \(title, description, identifier, creator, date etc.\)
* The [W3C Data Catalog Vocabulary](https://www.w3.org/TR/vocab-dcat/), a metadata model to describe different entities relevant to data sharing \(catalog, dataset, distribution\) and their relations
* The [Multi-Crop Passport Descriptors](https://en.wikipedia.org/wiki/Multi-Crop_Passport_Descriptor) a widely used international standard to facilitate germplasm passport information exchange developed jointly by IPGRI and FAO.

Examples of value vocabularies, or KOS, are:

* [AGROVOC](http://aims.fao.org/vest-registry/vocabularies/agrovoc), a controlled vocabulary covering all areas of interest of the Food and Agriculture Organization \(FAO\) of the United Nations, including food, nutrition, agriculture, fisheries, forestry, environment etc.
* [GeoNames](https://www.geonames.org/about.html), an authoritative database of geographic entities \(it covers 645 geographic features, among which countries, regions, administrative divisions, physical features like lakes, rivers, mountains…\)

A combination of metadata vocabulary and value vocabulary are ontologies, that define the complete set of metadata element and controlled values/entities that should be used to describe and classify specific “things”. Examples of ontologies are:

* The [Crop Ontology](https://www.cropontology.org/), which compiles validated concepts along with their inter-relationships on anatomy, structure and phenotype of crops, on trait measurement and methods as well as on germplasm with the multi-crop passport terms.
* The [Semantic Sensor Network \(SSN\) ontology](https://www.w3.org/TR/vocab-ssn/), an ontology for describing sensors and their observations, the involved procedures, the studied features of interest, the samples used to do so, and the observed properties, as well as actuators.

Besides “vocabularies”, other terms that are used for defining these resources are ‘semantic resources’ or ‘semantic structures’.

![Figure 3 Example of use of different types of vocabularies to add semantics to \(meta\)data](../.gitbook/assets/image%20%2813%29.png)

### 5.2.   How to identify the most suitable published vocabularies

To discover what published vocabularies are available, the most useful source of information are of course catalogues that are dedicated to the agri-food domain, but general catalogues searchable by domain can also be of help. An important distinction is to be drawn between catalogues/directories/registries on the one hand and repositories on the other: registries are conceived as metadata catalogues, providing descriptions and categorisation of vocabularies and linking to the original website and original serialisation of the standard, while repositories host the full content of the vocabulary, so that the terms themselves can be browsed. Below is an overview of some existing catalogues/repositories of data standards and vocabularies.

**Agri-food domain**

* GODAN Action Map of data standards - [http://vest.agrisemantics.org](http://vest.agrisemantics.org/)   A catalogue of data standards of different types and formats for the agri-food domain, categorised according to sub-domain, types of data, format and other criteria.
* AgroPortal - [http://agroportal.lirmm.fr/](http://agroportal.lirmm.fr/)  A repository of ontologies and value vocabularies, specialised in agronomy and food.
* Planteome - [http://browser.planteome.org/amigo](http://browser.planteome.org/amigo)  A repository of ontologies for plant biology.

**General**

* FAIRsharing - [https://fairsharing.org/](https://fairsharing.org/)  Evolved from the Biosharing directory of standards for life sciences, it is now a general directory of data standards of different types. It has a good tagging system but the coverage of agri-food standards is still poor.
* Linked Open Vocabularies \(LOV\) - [https://lov.okfn.org/dataset/lov](https://lov.okfn.org/dataset/lov)  Directory of RDF vocabularies spanning across all disciplines. It is not organised by domain or discipline and vocabularies can only be browsed through a small number of free tags.
* The Basel Register of Thesauri, Ontologies and Classifications \(BARTOC\) - [http://bartoc.org/](http://bartoc.org/)  BARTOC includes all types of KOS in any format, across all subject areas. The categorisation of vocabularies is quite generic \(food and agriculture would fall partly under pure science and partly under technology without further sub-categorisations\).

Besides choosing a vocabulary suitable for the data you manage, some other criteria are useful for selecting the most appropriate vocabulary:

* The ideal implementation of the ‘[Semantic Web](https://www.w3.org/standards/semanticweb/)’ is through namespaces, URIs and the [Linked Data](https://www.w3.org/standards/semanticweb/data) approach: in order to be able to exploit these technologies, it is preferable to choose vocabularies that have been published as RDF \(XML can be a good option too\) and follow the Linked Data approach \(use URIs, link to other vocabularies\).
* It is preferable to choose vocabularies that are widely used, so that your data is interoperable with more datasets and more systems.

If existing vocabularies do not meet your needs, you may decide to create your own vocabulary and publish it \(ideally, in collaboration with other partners in your community so as to ensure wide adoption\).

### 5.3.   Embedding semantics in the \(meta\)data

Semantic interoperability can be achieved at different levels and the implementation is different depending on the data format you’re using and the use you want to make of the vocabulary.

#### 5.3.1. Using a schema for your metadata

If you identify a metadata vocabulary/schema that has the classes and properties that you need to describe your data, you can reuse it to model and represent your data.

An important thing to note about using an existing published schema is that by doing this alone your data will be already more semantically interoperable, because instead of local metadata element names which are meaningless for a computer, you will use element names from a published vocabulary, and software tools that are aware of that vocabulary will be able to do something with it, e.g. match the values with values from other datasets that use the same schema.

The adopted schema becomes the “language” of your data structure: for instance, instead of using a custom XML structure with local element names, by adopting an existing XML schema you declare that you’re using elements from it and for each element you will use the element name of the selected schema instead of a local one, with a prefix that indicates from which schema the element comes.

The agreed way to show in your metadata that an element is coming from a published vocabulary is to add a prefix that identifies the vocabulary. In XML and in RDF-compliant formats like JSON-LD, prefixes can be associated with the URI of the vocabulary, so that the reference to the vocabulary is explicit. In other formats, like CSV, there may be no other way than just using conventional prefixes before column names \(or the full URI of the vocabulary before the property name, but this is not very practical for column names\).

In the example below, an XML file defines the prefixes for all the vocabularies \(schemes\) it will use; the om: prefix refers to the ISO data standard for Observations and Measurements \(O&M\):

```text
<om:OM_Observation
xmlns:om="http://www.opengis.net/om/2.0"
xmlns:gml="http://www.opengis.net/gml/3.2"
xsi:schemaLocation="http://www.opengis.net/om/2.0 
http://schemas.opengis.net/om/2.0/observation.xsd">
```

After the definition of the prefixes, every time the om: prefix is used, machines know that the following property name comes from the O&M vocabulary:

#### 5.3.2.  Using value vocabularies for your data

A slightly different case is when you want to use values from an existing vocabulary as values \(not metadata/properties\) in your dataset, for instance if you want to use the AGROVOC term for Oryza sativa or the term identifying a country from the FAO Geopolitical Ontology, in order to use unambiguous values across systems.

As a minimum, once some suitable vocabulary has been identified, if the vocabulary doesn’t use URIs and/or the URIs cannot be used in the dataset, at least the literal values of the terms can be used in the dataset: systems that are aware of the vocabulary and can match the literal against the URI can already do something with this.

Preferably, you should use the URI of the term you want to refer to.

Again, you can do it in different ways depending on the data format you are using.  
 In non-RDF XML or in CSV or in JSON, you can use the URI as the value of the element/column/label \(e.g. in XML you can use the URI of the Geopolitical Ontology country as the value of the dc:spatial element, perhaps specifying the scheme=”URI” attribute to make it clear it’s a URI\).

Ideally, semantic interoperability is fully achieved using an RDF-enabled serialization format \(XML/RDF, Turtle, N3, JSON-LD\). The advantage of using RDF is that RDF parsers and crawlers would normally look up additional properties from the URI address so you may not need to include redundant values in your data.

Even if you don’t find the ideal vocabulary that meets your needs and resort to using your own terms, you can link your local term to some similar or broader term in existing vocabularies

Using again the same XML example as above, the name of the dimension \(Temperature\) is taken from a NASA controlled vocabulary of property names, using the full URI, while the fact that the value is a measure is indicated using the MeasureType value from the Open Geospatial Consortium GML controlled vocabulary:

![Figure 4 Example of use of prefixes or URIs to refer to values defined in external vocabularies](../.gitbook/assets/image%20%2814%29.png)

The next lesson will show more examples, focusing on interoperability of farm data.

## Summary

This lesson illustrated the three layers of interoperability: infrastructural, structural and semantic.

For infrastructural interoperability, a quick overview of common protocols for data sharing like OAI-PMH, SPARQL and OPeNDAP was provided.

For structural interoperability, the features of the main file formats were highlighted especially in terms of ease of parsing by machines and suitability for semantic technologies.

Finally, for semantic interoperability, the lesson described more in depth the various types of vocabularies that can be used to semantically enrich data: metadata/description vocabularies, like schemas and metadata element sets, and value vocabularies, like thesauri or code lists.

The next lesson will provide some examples of data interoperability in practice, focusing on farm data.

## Bibliography

Tom Heath and Christian Bizer \(2011\) Linked Data: Evolving the Web into a Global Data Space \(1st edition\). Synthesis Lectures on the Semantic Web: Theory and Technology, 1:1, 1–136. Morgan & Claypool, San Rafael, CA, USA. Available online at: [http://linkeddatabook.com/editions/1.0/](http://linkeddatabook.com/editions/1.0/)

Antoniou, G., and van Harmelen, F. \(2003\). A Semantic Web Primer. MIT Press, Cambridge, MA, USA. Available online at: [http://www.csd.uoc.gr/~hy566/SWbook.pdf](http://www.csd.uoc.gr/~hy566/SWbook.pdf)

W3C. Semantic Web. [https://www.w3.org/standards/semanticweb/](https://www.w3.org/standards/semanticweb/)  

W3C. Data on the Web Best Practices. [https://www.w3.org/TR/dwbp/](https://www.w3.org/TR/dwbp/)

## Footnotes

‌\[1\] ‘Representational state transfer \(REST\) or RESTful web services is a way of providing interoperability between computer systems on the Internet. REST-compliant Web services allow requesting systems to access and manipulate textual representations of Web resources using a uniform and predefined set of stateless operations.’ From Wikipedia: [https://en.wikipedia.org/wiki/Representational\_state\_transfer](https://en.wikipedia.org/wiki/Representational_state_transfer)

