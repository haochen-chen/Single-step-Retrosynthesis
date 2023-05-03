# Single-step-Retrosynthesis
## Template-Based Methods
| Paper                                                   | Representation | Year | Journal / Conference | Code | Architecture/ Algorithm | Model | **USPTO—50K** |  |  | Data-source | **USPTO-MIT** |  |  | Data-source | **USPTO-Full** |  |  | Data-source |
| ------------------------------------------------------- | -------------------------------- | --------------------------------------- | --------------------------- | ------------------------- | --- | --- | --- | --- | --- |--- | --- | --- |--- | --- | --- | --- | --- | --- |
| |  |  |  |  | | | **K = 1** | **3** | **5** | |**K = 1** | **3** | **5** | | **K = 1** | **3** | **5** | |
| Neural-Symbolic Machine Learning for Retrosynthesis and Reaction Prediction    | Molecular Fingerprint | 2017 | ChemistryA European Journal | [pytorch](https://github.com/linminhtoo/neuralsym) | Highway network | Neuralsym | 38.7 | 56.2 | 62.2 | AutoSynRoute | 47.8 | 67.6 | 74.1 | AutoSynRoute |  35.8 | | | MEGAN |
| Computer-Assisted Retrosynthesis Based on Molecular Similarity    | Molecular Fingerprint | 2017 | ACS Central Science | [link](https://github.com/connorcoley/retrosim)  | Molecular similarity | Retrosim | 37.3 | 54.7 | 63.3 | | | | | | 32.8 |   | | RetroPrime |
| Prediction and Interpretable Visualization of Retrosynthetic Reactions Using Graph Convolutional Networks | Molecular Graph                 | 2019 | JCIM                         |    - |  GNN  | GCN |  24.9 |  | | | | | | |  |   | |  |
| Retrosynthesis Prediction with Conditional Graph Logic Network |  Molecular Graph                 | 2019 | NIPS                         | [pytorch](https://github.com/Hanjun-Dai/GLN) | GNN | GLN | 52.5 | 69.0 | 75.6 | | | | | | 39.3 | | |  RetroPrime|

## Reactant-Based Methods
| Paper                                                        | Representation        | Year | Journal / Conference         | Code                                                         |
| ------------------------------------------------------------ | --------------------- | ---- | ---------------------------- | ------------------------------------------------------------ |
| Bayesian Algorithm for Retrosynthesis | SMILES | 2020 | JCIM | [pytorch](https://github.com/zguo235/bayesian_retro)                    |
| RetCL: A Selection-based Approach for Retrosynthesis via Contrastive Learning | Graph  |       2021  |    IJCAI       |[pytorch](https://github.com/hankook/RetCL)    |


## Template-Free Generation
| Paper                 | Representation | Year | Journal / Conference | Code | Architecture/ Algorithm | Model | **USPTO—50K** |  |  | Data-source | **USPTO-MIT** |  |  | Data-source | **USPTO-Full** |  |  | Data-source |
| -------------------------------------- | -------------------------------- | --------------------------------------- | --------------------------- | ------------------------- | --- | --- | --- | --- | --- |--- | --- | --- |--- | --- | --- | --- | --- | --- |
| |  |  |  |  | | | **K = 1** | **3** | **5** | |**K = 1** | **3** | **5** | | **K = 1** | **3** | **5** | |
| Retrosynthetic Reaction Prediction Using Neural Sequence-toSequence Models    | SMILES | 2017 | ACS Central Science | [tensorflow](https://github.com/pandegroup/reaction_prediction_seq2seq) | LSTM | seq2seq |  28.3 | 42.8 | 47.3 | AutoSynRoute |  46.9 | 61.6 | 66.3 | AutoSynRoute |  | |   | |
| A Transformer Model for Retrosynthesis   | SMILES | 2019 | ICANN | [tensorflow](https://github.com/bigchem/retrosynthesis)      |  transformer | Transformer |  42.7 | 63.9 | 69.8 |  |  53.8 | 70.5 | 75.3 | a | 44.7 | 61.1 |  66.0  | a |
|  Predicting Retrosynthetic Reactions Using Self-Corrected Transformer Neural Networks | SMILES | 2020 | JCIM | [pytorch](https://github.com/yuedongyang/SCROP)      |  transformer | SCROP |  43.7 | 60.0 | 65.2 |  |  41.5 | 53.3 | 56.7|  | | |    |  |
| Automatic Retrosynthetic Route Planning Using Template-Free Models | SMILES            | 2020 | Chemical Science                         | [tensorflow](https://github.com/PKUMDL-AI/AutoSynRoute)      | transformer | AutoSynRoute | 43.1 | 64.6 | 71.8 | | 54.1 | 71.8 | 76.9 |


##未分类
| Paper                 | Representation | Year | Journal / Conference | Code | Architecture/ Algorithm | Model | **USPTO—50K** |  |  | Data-source | **USPTO-MIT** |  |  | Data-source | **USPTO-Full** |  |  | Data-source |
| -------------------------------------- | -------------------------------- | --------------------------------------- | --------------------------- | ------------------------- | --- | --- | --- | --- | --- |--- | --- | --- |--- | --- | --- | --- | --- | --- |
| |  |  |  |  | | | **K = 1** | **3** | **5** | |**K = 1** | **3** | **5** | | **K = 1** | **3** | **5** | |
| Learning to Make Generalizable and Diverse Predictions for Retrosynthesis | SMILES-            | 2020 | Computer Science                         |      |
