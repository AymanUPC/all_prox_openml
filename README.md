# Proximity Mining for Holistic Schema Matching Recommendation in the Data Lake (OpenML implementation)
This page is dedicated for the Proximity Mining for Holistic Schema Matching Recommendation in Data Lakes project by the [DTIM Research Group](http://www.essi.upc.edu/dtim) of the ESSI department, UPC. We provide here the main datasets and sources for experimental evaluation of our techniques on [OpenML](https://www.openml.org) data.



## Getting Started

We provide the annotated ground-truth used in our experiments for building the attribute-level proximtiy models (OML01 - The attribute-level annotated 15 DS) under the folder "OML01" and the dataset-level proximity models (OML02 - The dataset-level annotated 203 DS) under the folder "OML02". We provide the main indexes and matching output in the Comma Separated Values (CSV) format. The description of the data files in each folder is as follows:

### OML01
The attribute-level proximity models training datasets consisting of 15 OpenML datasets and the descriptions of the datasets and their attributes.
* **openml_15ds_datasets_index.csv:** The description of the OpenML datasets, the OpenML ID and the meta-features collected about the datasets using the data profiling techniques. Each row is a dataset from OpenML.
* **openml_15ds_attributes_nominal_index.csv:** A description of the nominal attributes in the 15 OpenML datasets. This includes the attribute name, dataset name and ID, the first 250 characters of values found in the attribute separated by a pipe '|' for each value (attr_values), and the meta-features collected about the attribute. Each row is an attribute from the 15 OpenML datasets used to train the attribute-level models.
* **openml_15ds_attributes_nominal_matching.csv:**  The matching of all nominal attribute pairs from the training datasets. This includes the names and IDs of both attributes and their datasets, the meta-features computed distances, the Levenshtein distance of the names of the attributes (name_dist), the similarity score assigned by the final proximity model (similarity_score), and whether both attributes have been annotated as matching attributes '1' or unmatching attributes '0' by the human annotators (attributes_match). Each row consists of an attribute pair from 2 different datasets.
* **openml_15ds_attributes_numeric_index.csv:** A description of the numeric attributes in the 15 OpenML datasets. This includes the attribute name, dataset name and ID, and the meta-features collected about the attribute. Each row is an attribute from the 15 OpenML datasets used to train the attribute-level models.
* **openml_15ds_attributes_numeric_matching.csv:**  The matching of all numeric attribute pairs from the training datasets. This includes the names and IDs of both attributes and their datasets, the meta-features computed distances, the Levenshtein distance of the names of the attributes (name_dist), the similarity score assigned by the final proximity model (similarity_score), and whether both attributes have been annotated as matching attributes '1' or unmatching attributes '0' by the human annotators (attributes_match). Each row consists of an attribute pair from 2 different datasets.

### OML02
The dataset-level proximity models training datasets consisting of 203 OpenML datasets and the descriptions of the datasets and their attributes.
* **openml_203ds_datasets_index.csv:** The description of the OpenML datasets and their OpenML ID, the manually annotated topic for the dataset by human annotators (dataset_topic), and the meta-features collected about the datasets using the data profiling techniques. Each row is a dataset from OpenML.
* **openml_203ds_datasets_matching.csv:** The matching of all dataset pairs. This includes the OpenML IDs and names of the datasets, the manually annotated topics for each dataset, and the meta-features computed distances, and whether both datasets in the pair have matching topics '1' or unmatching topics '0' (matching_topic). Each row consists of a dataset pair of 2 different datasets.
* **openml_203ds_attributes_nominal_index.csv:** A description of the nominal attributes in the 203 OpenML datasets. This includes the attribute name, dataset name and ID, the first 250 characters of values found in the attribute separated by a pipe '|' for each value (attr_values), and the meta-features collected about the attribute. Each row is an attribute from the 203 OpenML datasets used to train the dataset-level models.
* **openml_15ds_attributes_numeric_index.csv:** A description of the numeric attributes in the 203 OpenML datasets. This includes the attribute name, dataset name and ID, and the meta-features collected about the attribute. Each row is an attribute from the 203 OpenML datasets used to train the dataset-level models.


To retrieve the original datasets from OpenML using the APIs provided by them and the dataset IDs from our CSV files, please refer to the [OpenML API guide](https://openml.github.io/OpenML/Java-guide/).


## Built With

* [Java OpenML API](https://www.openml.org/guide#!java)
* [Postgres DB](https://www.postgresql.org/)
* [WEKA Machine Learning Environment](http://www.cs.waikato.ac.nz/ml/weka/)
* [Apache Lucene](http://lucene.apache.org/)

## License

This project is licensed under the Apache License 2.0 License - see the [LICENSE.md](LICENSE) file for details.

## Acknowledgements
We are sincerely thankful to all the annotators who have validated and collaborated in creating the ground-truth datasets for the experiments. We thank the collaborators from the school of Pharmacy for helping us with the annotation of the datasets.
