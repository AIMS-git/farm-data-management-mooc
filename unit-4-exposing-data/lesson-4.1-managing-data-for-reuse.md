# Lesson 4.1 Managing Data for Reuse

## Learning outcomes

At the end of this lesson, learners will \(be able to\):

* Identify the steps to ensure that good data management practices are followed
* Prepare a data management plan
* Understand management differences between static and dynamic datasets

## 1.   Introduction

The previous Unit gave an overview of how to use data. This Unit focuses on how to expose data so that other actors can reuse it.

Data cannot be exposed in an effective way and be of real use if it is not managed appropriately. For example:

* If weather data is not collected and stored according to specific temporal and spatial criteria or is not annotated with source and methodology information, it will be difficult to expose it selectively based on the needs of the users.
* If a database of farmer profiles is not regularly updated, users will not trust it; and if it is not regularly checked for consistency \(e.g. of values entered by different enumerators\), the data will not be sufficiently harmonized for reuse.

This is why the first lesson of this Unit is dedicated to data management.

Since this course is addressed to farmers and professionals working for farmers, data management is a relevant topic as far as specific data services are concerned, such as on-farm information systems/precision agriculture, data services for farmers, farmer profiling systems and the like. It is not expected that the building and maintenance of big public open data repositories is of high interest to the audience of this course, so this lesson does not go into the details of open data repository management practices or open data lifecycles.

While many of the recommendations in this lesson can be useful to all types of services provided to farmers, some are especially tailored to those services that collect large amounts of data \(either directly or from other sources\) and need to manage several datasets with challenges like dynamicity of data, multiple versions, licensing and usage rights issues etc.

Good data management is essential to enable users to expose quality data to: \(a\) other actors for reuse, for instance farm soil data, weather data or price data exposed to farm management information systems; \(b\) other parts of the system in complex distributed systems, for instance where weather data is used in precision agriculture equipment.

The main reason for anybody to reuse data – for example to provide services on top of a farmer profile – is that the data is trusted and useful/usable. Trust and usefulness have to do with the reliability of the data \(and the data source\), its quality and timeliness. Usability has to do with discoverability, ease of access, interoperability and documentation. Technical aspects of interoperability that are mentioned in this lesson \(like metadata and data standardization\) will be analyzed in more detail in the next two lessons.

After an overview of good practices in data management, including an indication of software tools that can help in managing and exposing data, this lesson illustrates the importance of having a data management plan and a data sharing policy.

Finally, this lesson provides some suggestions on how to maximise the use of a data service, in particular how to engage users.

## 2.   Good data management

In order to build and maintain trust in data, it is necessary to have stable data management principles and practices in place. Good data management principles help to ensure that data produced or used are registered, stored, made accessible for use and reuse, managed over time and/or disposed of, according to legal, ethical and funder requirements and good practice. For open data consumers, trust depends on numerous factors:

* Knowing the source. Trust in data begins with knowledge of its source.
* Trusting the source. If you know that data comes from a trusted source, then you can rely on it, and on the conclusions you draw from it.
* Timeliness of the data. Even when from a trusted source, data is not useful if it is outdated.
* Data quality. Trusted data must accurately and precisely reflect what it measures.
* Sustainability. A trusted dataset must have some guarantee of availability.
* Discoverability. Like documents, data is only useful if it is straightforward to find.
* Documentation and support. Consumers should be able to access support for data if needed.
* Interaction. Consumers should be able to provide feedback if there is a problem with data.

Data management, therefore, is a process involving a broad range of activities from administrative to technical aspects of handling data in a manner that addresses the factors listed above.  A sound data management policy will define strategic long-term goals for data management across all aspects of a project or enterprise.

A data management policy is a set of high-level principles that establish a guiding framework for data management. A data management policy can be used to address strategic issues such as data access, relevant legal matters, data stewardship issues and custodial duties, data acquisition, and other issues. As it provides a high-level framework, the data management policy should be flexible and dynamic. This allows for it to readily adapt to unanticipated challenges, different types of projects and potentially opportunistic partnerships while still maintaining its guiding strategic focus. The data management policy will help inform and develop a data management plan, which will be discussed more in this lesson.

In order to meet data management goals and standards, all involved parties must understand their associated roles and responsibilities. The objectives of delineating data management roles and responsibilities are to:

* clearly define roles associated with functions
* establish data ownership throughout all phases of a project
* instil data accountability
* ensure that adequate, agreed-upon data quality and metadata metrics are maintained on a continuous basis.

### 2.1. Data quality and consistency

Quality as applied to data has been defined as fitness for use or potential use. Many data quality principles apply when dealing with species data and with the spatial aspects of those data. These principles are involved at all stages of the data management process, beginning with data collection and capture. A loss of data quality at any one of these stages reduces the applicability and uses to which the data can be adequately put.

All of these affect the final quality or fitness for use of the data and apply to all aspects of the data. Data quality standards may be available for:

* accuracy
* precision
* resolution
* reliability
* repeatability
* reproducibility
* currency
* relevance
* ability to audit
* completeness
* timeliness.

Data quality is assessed by applying verification and validation procedures as part of the quality control process. Verification and validation are important components of data management that help ensure data is valid and reliable.

**Consistency**

Consistent data is data that is technically correct and fit for statistical analysis. This is data that has been checked for missing values, special values, \(obvious\) errors and outliers, which are either removed, corrected or imputed. The data is consistent with constraints based on real-world knowledge about the subject that the data describes.

Data quality is assessed by applying verification and validation procedures as part of the quality control process.

### 2.2. Cataloguing: metadata and content standardization

All datasets should be identified and documented to facilitate their subsequent identification, proper management and effective use, and to avoid collecting the same data more than once. To provide an accurate list of datasets held by an organisation, a catalogue of data should be compiled. This is a collection of discovery-level metadata for each dataset, in a form suitable for users to reference. These metadata should provide information about the content, geographic extent, currency and accessibility of the data, together with contact details for further information about the data.

All datasets, once catalogued, should also be documented in a detailed form suitable for users to reference when using the data. These detailed metadata should describe the content, characteristics and use of the dataset, using a standard detailed metadata template.

More technical explanations and examples are given in lessons 4.3 and 4.4.

**Metadata**

Metadata, or ‘data about data’ explains your dataset and allows you to document important information for:

* finding the data later
* understanding what the data is later
* sharing the data \(both with collaborators and future secondary data users\).

It should be considered an investment of time that will save you trouble later several-fold.

There are several useful vocabularies that have been created in order to use standardized common terms for metadata: examples are:

* Dublin Core \(for any information resource, including datasets\)
* Darwin Core \(for biological resources\)
* FGDC \(Federal Geographic Data Committee, for geographic metadata\)
* DDI \(Data Documentation Initiative, for datasets\)
* DCAT \(Data Catalog vocabulary, for datasets\)
* ABCD \(Access to Biological Collections Data, for germplasm databases\)
* CSDGM \(Content Standard for Digital Geospatial Metadata, for geographic metadata\).

See Lessons 4.3 and 4.4 for more information and examples on the use of metadata.

**File content standardization**

In order for others to use the data, they must understand the contents of the dataset, including the parameter names, units of measure, formats, and definitions of coded values. At the top of the file, include several header rows containing descriptors that link the data file to the dataset \(for example, the data file name, dataset title, author, today‘s date, the date the data within the file was last modified, and companion file names\). Other header rows should describe the content of each column, including one row for parameter names and one for parameter units. For those datasets that are large and complex and may require a lot of descriptive information about dataset contents, that information may be provided in a separate linked document rather than as headers in the data file itself.

* Parameters. The parameters reported in datasets need to have names that describe their contents, and their units need to be defined so that others understand what is being reported. Use commonly accepted parameter names. A good name is short, unique \(at least within a given dataset\), and descriptive of the parameter contents. Column headings should be constructed for easy importing by various data systems. Use consistent capitalisation and use only letters, numerals, and underscores – no spaces or decimal characters – in the parameter name. Choose a consistent format for each parameter and use that format throughout the dataset. When possible, try to use standardised formats, such as those used for dates, times, and spatial coordinates.
* Data type. All cells within each column should contain only one type of information \(e.g., text, numbers, etc.\). Common data types include text, numeric, date/time, Boolean \(Yes/No or True/False\), and comments \(used for storing large quantities of text\). 
* Coded Fields. Coded fields, as opposed to free text fields, often have standardised lists of predefined values from which the data provider may choose. Data collectors may establish their own coded fields with defined values to be consistently used across several data files. Coded fields are more efficient for the storage and retrieval of data than free text fields.
* Missing Values. There are several options for dealing with a missing value. One is to leave the value blank, but this poses a problem as some software does not differentiate a blank from a zero, or a user might wonder if the data provider accidentally skipped a column. Another option is to put a period where the number would go. This makes it clear that a value should be there, although it says nothing about why the data is missing. One more option is to use different codes to indicate different reasons why the data is missing. ****

**Version control**

It is important to identify and distinguish versions of datasets consistently. This ensures that a clear audit trail exists for tracking the development of a dataset and identifying earlier versions when needed. Thus you will need to establish a method that makes sense to you that will indicate the version of your dataset:

* A common form for expressing data file versions is to use ordinal numbers \(1, 2, 3, etc.\) for major version changes and decimals for minor changes \(e.g., v1, v1.1, v2.6\)
* Confusing labels should be avoided e.g. revision, final, final2, definitive copy, as you may find that these accumulate
* Record ALL changes \(minor and major\)
* Discard or delete obsolete versions \(whilst retaining the original 'raw' copy\)
* Use an auto-backup facility \(if available\) rather than saving or archiving multiple versions
* Turn on versioning or tracking in collaborative documents or storage utilities such as Wikis, GoogleDocs etc
* Consider using version control software e.g. Subversion, TortoiseSVN.

**Security and storage**

Effective data sharing depends on a strong network of trust between data providers and consumers. Infrastructure for data sharing will not be used if the parties who provide and use the data do not trust the infrastructure or one another. If sensitive data is to be shared, there must be provisions in the platform to ensure security of that data. Whether data is closed or shared with specific individuals or organisations, it will need to be hosted in a controlled way. Depending on the sensitivity of the data, this will include some guarantee of security, e.g. against hacking. In the most extreme cases, the security requirements for shared data in agriculture could be as severe as for shared data in the military. These principles are not unique to agricultural data and have been studied in depth.

The basic concepts behind these principles are that services should be hard to compromise, that a compromise should be easy to detect, and that the impact of a compromise can be contained. For open data, this is much less of a concern, but to build trust among data providers, some support for data security must be in place.

### 2.3. Data access and dissemination

Data production is one thing, its dissemination is another. Open data is useful when it can be delivered into the right hands \(or the right machine\) and within a context where it can be most valuable. In typical use cases of data for farmers, data is reused and delivered \(through intermediaries\) into the field, so it can be used to help farmers make informed decisions on which crop varieties to grow or which treatments to apply. There must be a variety of data delivery channels, fine-tuned to each case for data delivery. The ‘fine-tuning’ of data delivery channels can become a business opportunity for data intermediaries in the case where the data is fully ‘open’. An intermediary can provide services to customise data delivery for the vast range of customers that might exist for the data. Open data creates the possibility of a marketplace, where alternative sources of relevant data are available.

To be made available, data has to be stored in a way that makes it accessible. Even in the modern era of cloud deployment, the data and applications are stored on some hardware somewhere, even if it is virtualised. A strategy for sharing data on a global scale must specify where it will be stored and what service level agreements \(SLAs\) will be maintained \(up time, throughput, access controls, etc\).

The following should strongly be considered when deciding how to disseminate data:

* access to the data should be provided in line with the organisation’s data policy and the national laws/acts on access to information
* access to data should be granted without infringing the copyright or intellectual property rights of the data or any statutory/departmental obligations.

### 2.4. Dynamic vs. static datasets

Dynamic data denotes data that is asynchronously changed as further updates become available. The opposite of this is static data, also referred to as persistent data, which is infrequently accessed and not likely to be modified. Dynamic data is different from streaming data in that there is not a constant flow of information; rather, updates may come at any time, with periods of inactivity in between.

The rise of digital agriculture is changing the way farmers manage their land and livestock, such as with satellite-driven geo-positioning systems and sensors that detect nutrients and water in soil. These technologies ultimately result in the collection of more dynamic data, which is processed automatically.

Static datasets are normally stored and catalogued as described in the previous chapters and are exposed/published as downloads from an FTP server or a website. This can be done using specialized dataset management tools that combine storage, cataloguing and publication \(see 1.6 below\), but normally entails the manual upload of the dataset and its subsequent versions.

Dynamic datasets instead require some more effective form of **data automation**. Data automation is the process of updating data on a data portal programmatically.

Data automation incudes the automation of the three steps that Extract, Transform, and Load the data \([Extract–Transform–Load](%20https://en.wikipedia.org/wiki/Extract,_transform,_load), ETL\):

* Extract: the process of extracting your data from one or many source systems
* Transform: the process of transforming your data into the necessary structure, such as a flat file format like a CSV; this could also include things like normalizing values or applying schemas
* Load: the process of loading the data into the final system, be it a data portal or the backend of an API for other machines.

Dynamic datasets are usually exposed though **APIs \(Application Programming Interfaces\)**.

APIs allow you to take data and functionality that may already be available on your website and make them available through a programmatic API that both web and mobile applications can use by just calling a URL. Then, instead of returning HTML to represent the information like a website would, an API returns data in a machine-readable format, like the Extensible Markup Language \(XML\) or JavaScript Object Notation \(JSON\).

Developers can then take this data and use it in web and mobile applications. However, XML and JSON are easily consumed by spreadsheets and other tools non-developers can use as well, making APIs accessible by potentially anyone.

The reason why dynamic datasets are better accessible via APIs is that when you call an API you don’t download a static file, but you query the data directly and get a file that is created “on the fly”.

[The Open Data Institute](https://theodi.org/guides/engaging-reusers) suggests that the technical documentation that you must provide with an API should include:

* format documentation about the data formats that you are providing, possibly including schemas for any vocabularies that you use;
* code lists that provide more details about each of the codes that are used within your data; one way to provide this information is to have a URL that provides documentation about each code and to link to that URL within the data;
* service documentation that describes the way any API that you provide works; this might include links to machine-readable service descriptions if applicable.

Equipped with this information, reusers should be able to understand the data that you are publishing and how to create applications that use it.

Examples of existing APIs relevant for agriculture:

* The [IFPRI Food Security Portal](http://www.foodsecurityportal.org) contains over 40 indicators related to food security, commodity prices, economics, and human wellbeing. Much of this data is available for every country in the world and goes back over 50 years. They draw from public, authoritative data sources like the World Bank, the FAO, UNICEF, and others, as well as their own data.
* The [OpenWeatherMap](http://www.openweathermap.org) collects data from professional and private weather stations and publishes it through an API for developers. Today they have more than 40,000 weather stations; most are professional stations which are installed in airports, large cities, etc.

### 2.5. Data management plans

The planning process for data management begins with a data planning checklist. A checklist later assists in the development of a data management plan. That checklist might include considering some or all of the following questions.

* What data will you collect or create, how will it be created, and for what purpose?
* How will you manage any ethical issues? How will you manage copyright and intellectual property rights issues?
* What file formats will be used? Are they non-proprietary, transparent and sustainable? What directory and file naming conventions will be used? Are there any formal standards that you will adopt? What documentation and metadata will accompany the data?
* How will the data be stored and backed up? How will you manage access and security? Who will be responsible for data management?
* Are there existing procedures that you will base your approach on? For example, are there institutional data protection or security policies to follow, or guidelines/best practices/codes of conduct?
* What is the long-term preservation plan for the dataset? For example, which data should be retained, shared, and/or preserved? How will you share the data, and are any restrictions on data sharing required?
* What resources will you require to deliver your plan? For example, are there tools or software needed to create, process or visualise the data?

It is important to note that data management plans must be continuously maintained and kept up-to-date throughout the course of a project or research.

## 3.   Data management/catalog software

Generally, a data repository serves as the centrepiece of an open data effort and serves as a central location to find data, a venue for standardising practices, and a showpiece of the use of that data. In a practical sense, a repository serves as a central, searchable place for people to find data. Some repository software will automatically convert data from one format to others, so even though you can only provide data in one format \(e.g., CSV\), it will generate XML, JSON, Excel, etc.

Some software will visualise datasets in the browser, letting people map, sort, search, and combine datasets, without requiring any knowledge of how-to program.

Some repository software allows syndication, permitting other organisations to automatically incorporate your own data \(e.g., a state transportation agency could gather up all localities' transportation data and republish it\).

Some repository software tools comply with existing metadata standards, although in most cases only with generic vocabularies like Dublin Core, rarely with published standards for data catalogs \(see some more information on this in lesson 4.3\).

Generally, repository software supports either uploading files to be stored in the repository or pointing the repository at an existing website address where the file lives.

If the tool has been designed to also facilitate collection of data in the field, it will probably have a data collection module, preferably optimized for mobiles.

To make a broad division, there are two types of data catalog software: third-party/cloud hosted or self-hosted \(to be deployed on a server\), and both can be either paid or free.

**Self-hosted, free, open source**

There are some excellent open source data repository programs that are solid options for technically savvy organisations, for organisations with a commitment to use the open source software, or for organisations with the budget to hire a consultant to deploy the software.

* CKAN: CKAN is nominally an initialism for ‘Comprehensive Knowledge Archive Network,’ but it is only ever referred to as CKAN. A creation of UK-based Open Knowledge, CKAN is the most commonly used open source data repository software. It is written in Python and is the standard-bearer for repository software. Lamentably, it is also known for being difficult to install, although Docker images have simplified this substantially. Users of CKAN include Data.gov and the National Oceanic and Atmospheric Administration, among many others. CKAN consultants include Open Knowledge, Ontodia, and Accela, in addition to many independent consultants. Paid CKAN hosts include Open Knowledge and Ontodia. Please check a CKAN demo site.
* DKAN: DKAN is a clone of CKAN, although it shares no code with CKAN – it has been rewritten in PHP, as a Drupal module. For an organisation that uses the Drupal content management system and also wants a data repository, DKAN is an especially good option. Users of DKAN include the US Department of Agriculture, among others. Please check a DKAN demo site.
* JKAN: JKAN is nominally based on CKAN, although it shares no code with it. JKAN was created by Tim Wisniewski, Philadelphia’s Chief Data Officer, as a data catalog powered by Jekyll. Note that JKAN is a data catalogue, not a repository, which is to say that it stores links to data and metadata about that data, but not the data itself. The data could be hosted on an FTP server, in-place on agency websites, in Amazon S3, in Dropbox, or anywhere else one might store a file for public access. Setting up a site takes just a few minutes. Please check a JKAN demo site.
* [Open Data Kit](https://opendatakit.org/) \(ODK\)
* [QGIS](https://qgis.org/en/site/), specialized for geospatial data

**Cloud-hosted, commercial**

For some organisations, commercial hosting is going to be a viable option. Paying somebody to host your own data requires little to no technical knowledge on the part of your organisation, and the host will hold your hand through the process. Your organisation will not have to provide any technical infrastructure \(e.g., servers\) or know how to program \(although some of these platforms also have a self-hosted version\). It is important however that you carefully consider the service level agreements.

* ArcGIS Open Data: ArcGIS Open Data is a new entrant in the field, having been released in late 2014. ArcGIS Open Data is included with an ArcGIS Online contract – because of the universality of that service among municipalities and states, it is effectively free for those existing customers. This makes it a very attractive option for governments with low levels of buy-in to an open data program, because it eliminates the cost of a data catalogue. ArcGIS Open Data is only available as hosted software – it is not possible to run an instance of it on your own servers.
* Junar: Junar provides platforms and packages for businesses, governments, NGOs, and academia with a focus on data collection and analysis. Junar is bilingual, supporting English and Spanish audiences. Their pricing is targeted at small- to medium-sized organisations, starting at around US$10,000. Junar’s demo site is available upon request.
* NuCivic Data: NuCivic Data is based on DKAN, which was created and is maintained by nücivic. They’re a mid-range provider, in terms of pricing – their rates are much lower than Socrata, but more expensive than, for example, Junar.
* CivicDashboards: Open data consulting firm Ontodia provides hosted CKAN under the CivicDashboards banner. They offer a free tier, for storing a small number of datasets. Their pricing is comparable with Junar’s.
* OpenDataSoft: OpenDataSoft is a French company that has moved into the US market recently. They offer a free tier \(up to 5 datasets, each of up to 20,000 records\).
* Socrata Open Data: Socrata is the major vendor in the open data repository space, with their Socrata Open Data platform. Socrata only offers hosted options – there is no way to run Socrata’s software on your own servers. It is both the most feature-rich and the most expensive option, with plans running into hundreds of thousands of dollars a year.

More oriented towards distributed data collection, especially through mobile phones:

* [ONA](https://ona.io/plans.html), with special features for data collection from smartphones and data visualizations. They also have a free plan.

**Cloud-hosted, free**

There are some options available for free hosting of open data repositories. \(Note that the above-listed open source options are also free, but require setup, a server, and maintenance time.\) Besides, there is often a free option for the lowest tier of service provided by paid hosted services like the ones mentioned above.

* DataHub: The Open Knowledge Foundation provides DataHub, a free, CKAN-based data host. It is a large, collective repository – users do not get their own site, although it is possible to list only one’s own data and share a URL that only lists those datasets.
* GitHub: GitHub isn’t really meant as a data repository, but it can serve as one. It has none of the niceties of proper repository software \(conversion of formats, retrieving data from remote URLs, etc.\), but it does offer previews of some types of data, publicly tracks changes, and is a reasonable place to store datasets. It does offer one significant advantage, which is that GitHub – unlike any other repository software – provides a mechanism for people to propose changes to your datasets, which you can accept or decline, if they spot mistakes or areas for enhancement.
* JKAN on GitHub: JKAN is designed to be deployed onto GitHub, where the resulting data catalogue can be hosted for free. In this way, GitHub can serve as a free host without sacrificing the niceties of a data catalogue.

More oriented towards distributed data collection, through flexible web forms:

* [Kobo toolbox](https://www.kobotoolbox.org/), a suite of tools for field data collection for use in challenging environments. Besides the cloud service, the tool can also be self-hosted using Docker.

## 4.   Data sharing policies

As briefly illustrated in lesson 2.1, data exists on a spectrum: it can be closed, shared, or open. Closed data can only be accessed by the owners or the contracting parties. Shared data can be accessed on specific conditions \(authentication, payment\). Open data is data that anyone can access, use and share. In the spectrum, there are intermediate solutions. Whatever the position in the spectrum, it is important that data sharing conditions are clarified in a data policy.

A growing number of public and private-sector organisations are adopting the open data approach and are drafting open data policies. However, in the agricultural value chain, data can’t always be fully open: we have seen in Unit 2 the sensitivities around various types of data shared in the value chain. In such cases, a data sharing policy is equally if not more important.

A good data sharing policy will increase the transparency of your organisation and ensure the best use of your data. The translation of your data strategy into a solid policy is of great importance to ensure its successful implementation. Some elements that will be in an open data policy may be different from the elements in a non-open data sharing policy, but the elements highlighted below can be a good starting point for any data sharing policy,

A good \(open\) data policy will include some general context that helps to define its scope, for example:

* a definition of the general data strategy \(whether it’s fully open or not\) – why it is important to the organisation and the reasons for defining a policy
* a general declaration of principles that should guide the release and reuse of the data
* an outline of the types of data collected by the organisation and whether they are covered by the policy
* references to any relevant legislation, policies or other guidance which also apply to the management and sharing of information with third parties.

And it will then consider the following elements:

* the approach to identifying and prioritising data for release: how will data be inventoried, reviewed and then released?
* privacy considerations: ensuring that personal information is not shared and recommending steps to mitigate, e.g. by undertaking privacy impact assessments or approaches to anonymisation
* data ownership, copyright, consent to reuse: especially important when reusing data collected from other actors \(see lessons 2.2 and 2.3 on farm data rights\)
* data licensing and reuse rights: this will include not only the licence under which data will be released, but also the importance of clearing rights during data collection
* data publishing standards: ensuring that data is shared in well structured, machine-readable formats, with clear metadata and documentation
* engaging with reusers: how the organisation will work with external stakeholders to help guide release of data and ensure it can be easily used
* measuring success: what metrics the organisation will use to measure whether the policy is successful and how these measures will be shared
* approach to consuming open data: for organisations that are reusing open data, guidance on how to identify high-quality datasets and ensure reuse rights are clear
* concrete commitments: what the organisation is committing to do, in concrete terms, over the timespan of the policy
* policy transparency: how the policy and the processes it describes will be reviewed based on feedback from stakeholders and lessons learned.

A policy document will not necessarily include detailed information on each of these areas, e.g. specific standards or release processes. It will instead focus on general principles that should be followed and which may inform the drafting of more detailed guidance for practitioners.

## 5.   Ensuring reuse of exposed data

Data and services built on data will only have an impact if they are used by actors in society to achieve some of their goals. In particular, data shared in agricultural value chains has to be reused by actors, ultimately the farmer, to achieve their business objectives, to improve the value chain itself and to ensure transparency for the public good.               

For commercial actors sharing \(selling\) data and services, acquiring users for their services is essential, but also public providers need to demonstrate that their data makes an impact.

Some recommendations on how to make data useful and reusable have been given already in section 1, especially regarding data quality. Those recommendations were inherent to the data, while other actions can be taken once the data is published to maximise its reuse.

The first recommendation is to engage with users to make sure the data meets their needs and they have all the information on how to use it. Building on [Tim Berners Lee’s Five Stars for Open Data](http://5stardata.info/en/), Tim Davies has developed a [five-star open data engagement model](http://www.opendataimpacts.net/engagement/). The model suggests five steps to engage with users that will ensure that shared data is reused: 

**★ Be demand driven**

* Are your choices about the data you release, how it is structured, and the tools and support provided around it based on community needs and demands?
* Have you got ways of listening to people’s requests for data, and responding with open data?

★ ★ **Put data in context**

* Do you provide clear information to describe that data you provide, including information about frequency of updates, data formats and data quality?
* Do you include qualitative information alongside datasets such as details of how the data was created, or manuals for working with the data?
* Do you link from data catalogue pages to analysis of the data that your organisation, or third parties, have already carried out with it, or to third-party tools for working with the data?

★ ★ ★ **Support conversation around data**

* Can people comment on datasets, or create a structured conversation around data to network with other data users?
* Do you join the conversations?
* Are there easy ways to contact the individual ‘data owner’ in your organisation to ask them questions about the data, or to get them to join the conversation?
*  Are there offline opportunities to have conversations that involve your data?

★ ★ ★ ★ **Build capacity, skills and networks**

* Do you provide or link to tools for people to work with your datasets?
* Do you provide or link to How To guidance on using open data analysis tools, so people can build their capacity and skills to interpret and use data in the ways they want to?
* Do you go out into the community to run skill-building sessions on using data in particular ways, or using particular datasets?
* Do you sponsor or engage with capacity building to help the community work with open data?

★ ★ ★ ★ ★ **Collaborate on data as a common resource**

* Do you have feedback loops so people can help you improve your datasets?
* Do you collaborate with the community to create new data resources \(e.g. derived datasets\)?
* Do you broker or provide support to people to build and sustain useful tools and services that work with your data?
* Do you work with other organisations to connect up your data sources.

Other useful suggestions for engaging with data users are:

* providing tools, such as plugins, visualisations, software libraries and services that enable reusers to build on others' work with the data \(these tools are sometimes built by third parties\)
* blogging to showcase good examples of use of your data
* arranging hackdays or competitions to encourage the use of your data
* Whilst not worthwhile for all datasets, in some cases explicit community building, engagement and outreach work can help to maximise the value that your data brings to your organisation and to others.

## 6.   Summary

This lesson provided the essential information for good management of data, primarily in the perspective of sharing data with other systems.

The key aspects of good data management that were presented are those that make the data relevant and trusted and therefore reused, from data quality and timeliness to its discoverability, documentation and interaction services. The lesson highlighted features that are related to sharing data, like metadata, content standardization, static and dynamic ways to expose data, APIs.

The importance of instruments like data management plans and data policies, and what should go there, was also illustrated. On a more practical note, some support tools for dataset management and dissemination were briefly presented and suggestions were given on how to engage users and ensure reuse of the data.

## Bibliography

Arms, C. R., Fleischhauer, C. and Murray, K. \(2013\). Sustainability of digital formats: planning for Library of Congress collections. Library of Congress, Washington DC, USA. Available at [www.digitalpreservation.gov/formats](http://www.digitalpreservation.gov/formats)

Beagrie, N. and Houghton, J. \(2014\). The value and impact of data sharing and curation - synthesis of three recent UK studies. Jisc, London, UK. Available online at: [http://www.repository.jisc.ac.uk/5568/1/iDF308\_-\_Digital\_Infrastructure\_Directions\_Report%2C\_Jan14\_v1-04.pdf](http://www.repository.jisc.ac.uk/5568/1/iDF308_-_Digital_Infrastructure_Directions_Report%2C_Jan14_v1-04.pdf)

Charles Beagrie Ltd \(2013\). Keeping research data safe: cost / benefit studies, tools, and methodologies focussing on long-lived data. Available at:  [http://www.beagrie.com/krds.php](http://www.beagrie.com/krds.php) \(accessed 4 August 2014\)

Digital Curation Centre \(DCC\). \(2010\). Data management plans. Available at: [http://www.dcc.ac.uk/resources/data-management-plans](http://www.dcc.ac.uk/resources/data-management-plans) \(accessed 4 August 2014\)

Drummond, C.G. \(2009\). Replicability is not reproducibility: nor is it good science. In Proceedings of the Evaluation Methods for Machine Learning Workshop, 26th ICML, Montreal, Canada. Available at: [http://cogprints.org/7691](http://cogprints.org/7691)

European Commission \(EC\). \(2017\). Guidelines to the Rules on Open Access to Scientific Publications and Open Access to Research Data in Horizon 2020. Available at:  ec.europa.eu/research/participants/data/ref/h2020/grants\_manual/hi/oa\_pilot/h2020-hi-oa-pilot-guide\_en.pdf \(Version 3.2, 21 March 2017\)

GODAN 2016 A Global Data Ecosystem for Agriculture and Food. GODAN, Wallingford, UK. Available at: http://www.godan.info/documents/data-ecosystem-agriculture-and-food

Jones, S. \(2011\). How to Develop a Data Management and Sharing Plan. DCC How-to Guides, Digital Curation Centre, Edinburgh, UK. Available at: [www.dcc.ac.uk/resources/how-guides/develop-data-plan](http://www.dcc.ac.uk/resources/how-guides/develop-data-plan)

UK Data Archive \(UKDA\). Plan to Share. Available at: [www.data-archive.ac.uk/create-manage/planning-for-sharing](http://www.data-archive.ac.uk/create-manage/planning-for-sharing) \(accessed 4 August 2014\)

## 

