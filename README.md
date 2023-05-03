# Single-step-Retrosynthesis
## Template-Based Methods

| Paper                 | Representation | Year | Journal / Conference | Code | Architecture/ Algorithm | Model | **USPTO—50K** |  |  | Data-source | **USPTO-MIT** |  |  | Data-source | **USPTO-Full** |  |  | Data-source |
| -------------------------------------- | -------------------------------- | --------------------------------------- | --------------------------- | ------------------------- | --- | --- | --- | --- | --- |--- | --- | --- |--- | --- | --- | --- | --- | --- |
| |  |  |  |  | | | **K = 1** | **3** | **5** | |**K = 1** | **3** | **5** | | **K = 1** | **3** | **5** | |
| Neural-Symbolic Machine Learning for Retrosynthesis and Reaction Prediction    | Molecular Fingerprint | 2017 | ChemistryA European Journal | [pytorch](https://github.com/linminhtoo/neuralsym) | Highway network | Neuralsym | 44.4 | 65.3 | 72.4 | GLN | 47.8 | 676.6 | 74.1 | AutoSynRoute |  35.8 | | | MEGAN |
| Computer-Assisted Retrosynthesis Based on Molecular Similarity    | Molecular Fingerprint | 2017 | ACS Central Science | [link](https://github.com/connorcoley/retrosim)  | Molecular similarity | Retrosim | 37.3 | 54.7 | 63.3 | | | | | | 32.8 |   | | RetroPrime |


## Template-Free Generation
| Paper                 | Representation | Year | Journal / Conference | Code | Architecture/ Algorithm | Model | **USPTO—50K** |  |  | Data-source | **USPTO-MIT** |  |  | Data-source | **USPTO-Full** |  |  | Data-source |
| -------------------------------------- | -------------------------------- | --------------------------------------- | --------------------------- | ------------------------- | --- | --- | --- | --- | --- |--- | --- | --- |--- | --- | --- | --- | --- | --- |
| |  |  |  |  | | | **K = 1** | **3** | **5** | |**K = 1** | **3** | **5** | | **K = 1** | **3** | **5** | |
| Retrosynthetic Reaction Prediction Using Neural Sequence-toSequence Models    | SMILES | 2017 | ACS Central Science | [tensorflow](https://github.com/pandegroup/reaction_prediction_seq2seq) | LSTM | seq2seq |  28.3 | 42.8 | 47.3 | AutoSynRoute |  46.9 | 61.6 | 66.3 | AutoSynRoute |  | |   | |

