# Proximity Mining for Holistic Schema Matching Recommendation in the Data Lake (OpenML implementation)
This page is dedicated for the Proximity Mining for Holistic Schema Matching Recommendation in Data Lakes project by the [DTIM Research Group](http://www.essi.upc.edu/dtim) of the ESSI department, UPC. We provide here the main datasets and sources for experimental evaluation of our techniques on [OpenML](https://www.openml.org) data.



## Getting Started

We provide the annotated ground-truth used in our experiments for building the attribute-level proximtiy models (OML01 - The attribute-level annotated 15 DS) under the folder "OML01" and the dataset-level proximtiy models (OML02 - The dataset-level annotated 203 DS) under the folder "OML02". We provide the main indexes and matching output as in the Comma Separated Values (CSV) format. The description of the datasets in each folder is as follows:

### OML01
The attribute-level proximity models training datasets consisting of 15 OpenML datasets and the descriptions of the datasets and their attributes.
* openml_15ds_datasets_index.csv: The description of the OpenML datasets, the OpenML ID and the meta-features collected about the datasets using the data profiling techniques. Each row is a dataset from OpenML.
* openml_15ds_attributes_nominal_index.csv: A description of the nominal attributes in the 15 OpenML datasets. This incldues the attribute name, dataset name and ID, and the meta-features collected about the attribute. Each row is an attribute from the 15 OpenML datasets used to train the attribute-level models.
* openml_15ds_attributes_nominal_matching.csv:  


* The "index" CSV files: They store the original index of datasets collected for the training set or the testing set in the experiments. It comes with the OpenML dataset ID, the dataset name, and the meta-features collected for each dataset.
* The "matching" CSV files: They store the meta-features' distances between all pairs of datasets in the training set or the testing set of the experiments. It comes with the OpenML dataset ID, the dataset name, the meta-features distances between the pair in each row, and the ground-truth of the relationships between the datasets in the pair: datesets_subject_main_match (1 or 0) for the Rel(d1,d2) relationship and datesets_duplicates_match (1 or 0) for the Dup(d1,d2) relationship.

### OML02


To retrieve the original datasets from OpenML using the APIs provided by them and the dataset IDs (did) from our CSV files, please refer to the [OpenML API guide](https://www.openml.org/guide).


## Built With

* [Java OpenML API](https://www.openml.org/guide#!java)
* [Postgres DB](https://www.postgresql.org/)
* [WEKA Machine Learning Environment](http://www.cs.waikato.ac.nz/ml/weka/)
* [Apache Lucene](http://lucene.apache.org/)

## License

This project is licensed under the Apache License 2.0 License - see the [LICENSE.md](LICENSE) file for details

## Acknowledgments
We are sincerely thankful to all the annototators who have validated and collaborated in creating the ground-truth datasets for the experiments. We thank the collaborators from the school of Pharmacy for helping us with the annotation of the datasets.
