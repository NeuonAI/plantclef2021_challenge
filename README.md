# Neuon AI in PlantCLEF 2021
This repository contains the team's work in [PlantCLEF 2021](https://www.aicrowd.com/challenges/lifeclef-2021-plant).
The goal of the challenge was to identify plants in field pictures based on a training set of digitized herbarium specimens. We achieved an MRR of 0.181 on the primary metric and an MRR of 0.158 on the secondary metric (difficult species). The official results are released [here](https://www.imageclef.org/PlantCLEF2021).

## Methodology
### Stage 1: Construct and train networks
#### Herbarium-Field Triplet Loss Network (HFTL Network)
![Figure 1](https://github.com/NeuonAI/plantclef2021_challenge/blob/65c1058d41fe7daad951c0e4fd9e92e0cee71208/figures/HFTL_network.png "Herbarium-Field Triplet Loss Network")

#### One-streamed Network (OSM Network)
![Figure 2](https://github.com/NeuonAI/plantclef2021_challenge/blob/65c1058d41fe7daad951c0e4fd9e92e0cee71208/figures/OSM_network.png "One-streamed Network")

### Stage 2: Obtain herbarium dictionary
#### Herbarium Dictionary Construction
![Figure 3](https://github.com/NeuonAI/plantclef2021_challenge/blob/65c1058d41fe7daad951c0e4fd9e92e0cee71208/figures/herbarium_dictionary.png "Herbarium Dictionary Construction")

### Stage 3: Compare feature similarity between field embedding and herbarium dictionary
### Feature similarity comparison
![Figure 4](https://github.com/NeuonAI/plantclef2021_challenge/blob/65c1058d41fe7daad951c0e4fd9e92e0cee71208/figures/feature_similarity.png "Feature similarity comparison")


## Repository files

### Training scripts
- **HFTL Network**
  - [run_HFTL_network.py](https://github.com/NeuonAI/plantclef2021_challenge/blob/65c1058d41fe7daad951c0e4fd9e92e0cee71208/run_HFTL_network.py) (Main script)
  - [network_module_HFTL.py](https://github.com/NeuonAI/plantclef2021_challenge/blob/65c1058d41fe7daad951c0e4fd9e92e0cee71208/network_module_HFTL.py) 
- **OSM Network**
  - [run_OSM_network.py](https://github.com/NeuonAI/plantclef2021_challenge/blob/65c1058d41fe7daad951c0e4fd9e92e0cee71208/run_OSM_network.py) (Main script)
  - [network_module_OSM.py](https://github.com/NeuonAI/plantclef2021_challenge/blob/65c1058d41fe7daad951c0e4fd9e92e0cee71208/network_module_OSM.py)

### Validation scripts
- **HFTL Network**
  - (1) [get_herbarium_dictionary_HFTL.py](https://github.com/NeuonAI/plantclef2021_challenge/blob/65c1058d41fe7daad951c0e4fd9e92e0cee71208/get_herbarium_dictionary_HFTL.py)
  - (2) [validate_HFTL_network.py](https://github.com/NeuonAI/plantclef2021_challenge/blob/65c1058d41fe7daad951c0e4fd9e92e0cee71208/validate_HFTL_network.py)
  - (3) [get_mrr_score.py](https://github.com/NeuonAI/plantclef2021_challenge/blob/65c1058d41fe7daad951c0e4fd9e92e0cee71208/get_mrr_score.py)

- **OSM Network**
  - (1) [get_herbarium_dictionary_OSM.py](https://github.com/NeuonAI/plantclef2021_challenge/blob/65c1058d41fe7daad951c0e4fd9e92e0cee71208/get_herbarium_dictionary_OSM.py)
  - (2) [validate_OSM_network.py](https://github.com/NeuonAI/plantclef2021_challenge/blob/65c1058d41fe7daad951c0e4fd9e92e0cee71208/validate_OSM_network.py)
  - (3) [get_mrr_score.py](https://github.com/NeuonAI/plantclef2021_challenge/blob/65c1058d41fe7daad951c0e4fd9e92e0cee71208/get_mrr_score.py)
 
### Lists
- **Herbarium Network**
  - Train <br /> [list/herbarium/clef2021_herbarium_combined_train_306005.txt](https://github.com/NeuonAI/plantclef2021_challenge/blob/65c1058d41fe7daad951c0e4fd9e92e0cee71208/list/herbarium/clef2021_herbarium_combined_train_306005.txt)
  - Test <br /> [list/herbarium/clef2021_herbarium_combined_test_15221.txt](https://github.com/NeuonAI/plantclef2021_challenge/blob/65c1058d41fe7daad951c0e4fd9e92e0cee71208/list/herbarium/clef2021_herbarium_combined_test_15221.txt)

- **Field Network (2017)**
  - Train <br /> [list/field_2017/clef2017_EOL_Web_train_server.txt](https://github.com/NeuonAI/plantclef2021_challenge/blob/65c1058d41fe7daad951c0e4fd9e92e0cee71208/list/field_2017/clef2017_EOL_Web_train_server.txt)
  - Test <br /> [list/field_2017/clef2017_EOL_Web_test_server.txt](https://github.com/NeuonAI/plantclef2021_challenge/blob/65c1058d41fe7daad951c0e4fd9e92e0cee71208/list/field_2017/clef2017_EOL_Web_test_server.txt)

- **Field Network (2021)**
  - Train <br /> [list/field_2021/clef2021_field_combined_train.txt](https://github.com/NeuonAI/plantclef2021_challenge/blob/65c1058d41fe7daad951c0e4fd9e92e0cee71208/list/field_2021/clef2021_field_combined_train.txt)
  - Test <br /> [list/field_2021/clef2021_field_combined_test.txt](https://github.com/NeuonAI/plantclef2021_challenge/blob/65c1058d41fe7daad951c0e4fd9e92e0cee71208/list/field_2021/clef2021_field_combined_test.txt)
 
- **HFTL Network**
  - Herbarium Train <br /> [list/HFTL/clef2020_known_classes_herbarium_train_added.txt](https://github.com/NeuonAI/plantclef2021_challenge/blob/65c1058d41fe7daad951c0e4fd9e92e0cee71208/list/HFTL/clef2020_known_classes_herbarium_train_added.txt) 
  - Herbarium Test <br /> [list/HFTL/clef2020_known_classes_herbarium_test.txt](https://github.com/NeuonAI/plantclef2021_challenge/blob/65c1058d41fe7daad951c0e4fd9e92e0cee71208/list/HFTL/clef2020_known_classes_herbarium_test.txt) 
  - Field Train <br /> [list/HFTL/clef2020_known_classes_field_train_added.txt](https://github.com/NeuonAI/plantclef2021_challenge/blob/65c1058d41fe7daad951c0e4fd9e92e0cee71208/list/HFTL/clef2020_known_classes_field_train_added.txt) 
  - Field Test <br /> [list/HFTL/clef2020_known_classes_field_test.txt](https://github.com/NeuonAI/plantclef2021_challenge/blob/65c1058d41fe7daad951c0e4fd9e92e0cee71208/list/HFTL/clef2020_known_classes_field_test.txt)

- **OSM Network**
  - Train <br /> [list/OSM/clef2021_mixed_class_train.txt](https://github.com/NeuonAI/plantclef2021_challenge/blob/65c1058d41fe7daad951c0e4fd9e92e0cee71208/list/OSM/clef2021_mixed_class_train.txt)
  - Test <br /> [list/OSM/clef2021_mixed_class_test.txt](https://github.com/NeuonAI/plantclef2021_challenge/blob/65c1058d41fe7daad951c0e4fd9e92e0cee71208/list/OSM/clef2021_mixed_class_test.txt)

- **Herbarium Dictionary**
  - Without field bias <br /> [list/997_class_emb_sample_for_herbDict_server_removed_duplicates.txt](https://github.com/NeuonAI/plantclef2021_challenge/blob/65c1058d41fe7daad951c0e4fd9e92e0cee71208/list/997_class_emb_sample_for_herbDict_server_removed_duplicates.txt)
  - With field bias <br /> [list/997_class_emb_sample_for_herbDict_new_field_bias.txt](https://github.com/NeuonAI/plantclef2021_challenge/blob/65c1058d41fe7daad951c0e4fd9e92e0cee71208/list/997_class_emb_sample_for_herbDict_new_field_bias.txt)
 
- **Test Sets**
  - Test Set 1 (With field training images) <br /> [list/HFTL/clef2020_known_classes_field_test.txt](https://github.com/NeuonAI/plantclef2021_challenge/blob/65c1058d41fe7daad951c0e4fd9e92e0cee71208/list/HFTL/clef2020_known_classes_field_test.txt)
  - Test Set 2 (Without field training images) <br /> [list/missing_class_sample.txt](https://github.com/NeuonAI/plantclef2021_challenge/blob/65c1058d41fe7daad951c0e4fd9e92e0cee71208/list/missing_class_sample.txt) <br />
  (Note: The [image files for Test Set 2](https://github.com/NeuonAI/plantclef2021_challenge/tree/main/planttest) are sourced from Google Image queries)


### Checkpoints
- **HFTL Network**
  - [HFTL inception v4 model](https://github.com/NeuonAI/plantclef2021_challenge/tree/main/checkpoints/HFTL_network)
- **OSM Network**
  - [OSM inception v4 model](https://github.com/NeuonAI/plantclef2021_challenge/tree/main/checkpoints/OSM_network)
