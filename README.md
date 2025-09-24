## Project Overview

This repository contains a pipeline for multiclass classification as a part of a bigger project. The BERT model HerBERT is pre-trained on Polish text data and is used for sequence classification.

The aim of this project is to check, which 'missing domain information' suggested by the Nuclear Domain Expert Agent has been adressed druging article refinement processed (pointed by the Refine Agent). To prepare the dataset, 'missing information' dataset has been grouped into 20 clusters and got 20 topic labels assigned. It serves as a golden labels now. We traine the classfier to mark the 'addressed missing information' dataset and check the distribution of the adressed problems.


## Dataset structure

- **Text**: Expert questions and information requests in Polish
- **Category**: Classification labels for different types of missing information (20 clusters)


### Data Files

- `addressed_missing_info_expert.csv` - Expert queries that have been addressed (2.2MB, but not classfied)
- `suggested_train_expert.csv` - Training data for suggested expert queries (2.3MB)
- `suggested_test_expert.csv` - Test data for suggested expert queries (295KB)
- `suggested_validation_expert.csv` - Validation data for suggested expert queries (301KB)

## Model Architecture

- **Base Model**: HerBERT (Polish BERT)
- **Task**: Multiclass text classification
- **Framework**: PyTorch with Transformers library
- **Device**: CUDA-enabled GPU support with CPU fallback


## File Structure

```
herbert_multiclass_classification/
├── README.md
├── .gitignore
├── polish_bert_expert_missing.ipynb    # Main training notebook
├── addressed_missing_info_expert.csv   # Addressed expert queries
├── suggested_train_expert.csv          # Training data
├── suggested_test_expert.csv           # Test data
└── suggested_validation_expert.csv     # Validation data
```

## Technical Details

- **Language**: Polish
- **Model Type**: BERT-based sequence classification
- **Input**: Raw Polish text
- **Output**: Classification probabilities for each category

