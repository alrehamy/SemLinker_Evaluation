# SemLinker Evaluation Datasets

SemLinker is an ontology based big data integration system for big data processing platforms which are expected to be operated by non-expert users, such as Personal Data Lake. SemLinker architecture is described in the research paper: "SemLinker: Automating Big Data Integration in the Personal Data Lake" (under review in EPJ Data Science Journal).

In this git, we describe how to we configured SemLinker during the experimental evaluations explained in the above paper. The git aims to provide detailed descriptions regarding the following:

# SemLinker Global Ontology
SemLinker utilizes schema.org as the backbone of its global schema (ontology). The file "schema.rdf" contains the full translation of schema.org taxonomy described in the official website. For up-to-date version, please check this URL (http://schema.org/docs/developers.html). At the time of designing the initial prototype of SemLinker, Schema.org version is v3.3.0.

 

The extra-data section contains a small set of triples to define the meta schema relations G:hesitated and G:hasProperty, as well as the data added to concepts described in the subsection section.


# Datasets
For SemLinker evaluation, we needed large number of high-volume datasets, where each dataset must meet two requirements: I) useable in personal data management context, ii) consists of relatively large number of attributes. Eventually, we limited our choice to 11 heterogeneous but semantically related datasets. For each dataset, we provide brief description about its contents; its attributes, few data samples, and what attributes we chosen for modeling (i.e. the partial unified view). Backbone, Twitter, Flickr, and Foursquare datasets are captured in realties API streaming, whereas, the rest of the datasets are publicly available online and can be accessed and downloaded using the following URLs:


https://archive.ics.uci.edu/ml/datasets/Heterogeneity+Activity+Recognition

https://hal.archives-ouvertes.fr/hal-01586802

https://www.kaggle.com/PromptCloudHQ/londonbased-restaurants-reviews-on-tripadvisor

http://tour-pedia.org/about/datasets.html

http://ratings.food.gov.uk/open-data/

https://www.getthedata.com/open-postcode-geo


The folder "Data" includes all the used datasets without any preprocessing. The usage of these datasets is subject to the license agreements provided by their authors.


The folder "Data" also contains information to describe how each dataset was tagged with a semantically corresponding ontological concept from schema.org, the mix collection of default properties provided by schema.org, as well as new extension properties we add to the used concepts (such as geo:latitude and geo:longitude). Information regarding how each ontological property is mapped to its semantically equivalent schema element in the particular dataset, are also provided here.



# Schema Evolution Simulations
The folder "Evolutions" contains information to describe how we simulated evolutions in the physical schema of each dataset during experiments design. The file "mappings.xlsx" contains the mappings between the elements of the (evolved) schema(s) of each dataset and their semantically equivalent ontological properties that have been computed automatically by SemLinker using three different schema matcher plugins.

