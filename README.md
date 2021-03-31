[![spaCy](https://img.shields.io/badge/built%20with-spaCy-09a3d5.svg)](https://spacy.io)
# medaCy
:hospital: Clinical Notes Model for medaCy (BERT) :hospital:

This repository contains a versioned, medaCy compatible Model for information extraction from clinical notes.

![alt text](https://nlp.cs.vcu.edu/images/Edit_NanomedicineDatabase.png "Nanoinformatics")

# Description
This is the light-weight version (no metamap) of medaCy's model for extracting 9 unique entities from clinical notes:

`Drug, Strength, Duration, Route, Form, ADE, Dosage, Reason, Frequency`

# Results
Model generalization ability is evaluated over 202 patient clinical note files not seen during training. *Strict* indicates exact matches of spans, *Lenient* indicates a fuzzy matching of spans (model predictions are off by single characters).

| Entity (Count)    |   Precision |   Recall |    F1 |   F1_Min |   F1_Max |
|-------------------|-------------|----------|-------|----------|----------|
| ADE (1584)        |       0.562 |    0.301 | 0.381 |    0.216 |    0.457 |
| Dosage (6902)     |       0.942 |    0.953 | 0.948 |    0.939 |    0.958 |
| Drug (26800)      |       0.904 |    0.891 | 0.897 |    0.891 |    0.904 |
| Duration (970)    |       0.833 |    0.821 | 0.825 |    0.779 |    0.862 |
| Form (11010)      |       0.93  |    0.941 | 0.936 |    0.924 |    0.954 |
| Frequency (10293) |       0.873 |    0.966 | 0.917 |    0.908 |    0.926 |
| Reason (6400)     |       0.663 |    0.528 | 0.586 |    0.563 |    0.612 |
| Route (8989)      |       0.933 |    0.924 | 0.928 |    0.916 |    0.939 |
| Strength (10921)  |       0.948 |    0.958 | 0.953 |    0.945 |    0.957 |
| system (83869)    |       0.893 |    0.9   | 0.895 |    0.889 |    0.901 |

# Training Data
N2C2 2018 Shared Task
The data used to induce this model is protected by HIPAA privacy regulations and thus cannot be published.

Authors
=======
Andriy Mulyar and Bridget McInnes

Acknowledgments
===============
- [VCU Natural Language Processing Lab](https://nlp.cs.vcu.edu/)     ![alt text](https://nlp.cs.vcu.edu/images/vcu_head_logo "VCU")
- [Nanoinformatics Vertically Integrated Projects](https://rampages.us/nanoinformatics/)
