# Single-step-Retrosynthesis

## Template-Based Methods 
| Paper                                                        | Year | Journal / Conference         | Code                                                                                 | 
| ------------------------------------------------------------ | ---- | ---------------------------- | ------------------------------------------------------------------------------------ | 
| Neural-Symbolic Machine Learning for Retrosynthesis and Reaction Prediction    | 2017 | ChemistryA European Journal | [pytorch](https://github.com/linminhtoo/neuralsym)                  |
| Computer-Assisted Retrosynthesis Based on Molecular Similarity                 | 2017 | ACS Central Science         | [link](https://github.com/connorcoley/retrosim)                     |
| Prediction and Interpretable Visualization of Retrosynthetic Reactions Using Graph Convolutional Networks | 2019    | JCIM  | -                                                           |
| Retrosynthesis Prediction with Conditional Graph Logic Network                 | 2019 | NIPS                        | [pytorch](https://github.com/Hanjun-Dai/GLN)                        |
| Data Augmentation and Pretraining for Template-Based Retrosynthetic Prediction in Computer-Aided Synthesis Planning | 2020  | JCIM           | [tensorflow](https://gitlab.com/mefortunato/template-relevance) |
| Self-Improved Retrosynthetic Planning                        | 2021  | ICML                        |     [pytorch](https://github.com/junsu-kim97/self_improved_retro)                    |
| ChemiRise: a data-driven retrosynthesis engine               | 2021  | -                           | -                                                                                    |
| Deep Retrosynthetic Reaction Prediction using Local Reactivity and Global Attention | 2021 | JACS Au                | [pytorch](https://github.com/kaist-amsg/LocalRetro)                 |
| Towards understanding retrosynthesis by energy-based models   | 2021 | NIPS                                 | -                                                                           |
| Improving Few- and Zero-Shot Reaction Template Prediction Using Modern Hopfield Networks | 2022 | JCIM              | [pytorch](https://github.com/ml-jku/mhn-react)                      |
| CNN‑based two‑branch multi‑scale feature extraction network for retrosynthesis prediction | 2022 | BMC Bioinformatics |  -                                                                |
| RetroComposer: Composing Templates for Template-Based Retrosynthesis Prediction | 2022 | Biomolecules | [pytorch](https://github.com/uta-smile/RetroComposer)                             |

|Architecture/ Algorithm | Representation | Model   | **USPTO-50K** |       |       | Datasource  | **USPTO-MIT**  |       |       | Datasource  | **USPTO-Full** |       |       | Datasource |
| ---------------------- | -------------- |-------- | ------------- | ----- | ----- | ----------- | -------------- | ----- | ----- | ----------- | -------------- | ----- | ----- | ---------- |
|                        |                |         | **K = 1**     | **3** | **5** |             | **K = 1**      | **3** | **5** |             | **K = 1**      | **3** | **5** |            |
| Highway network        | Molecular Fingerprint | Neuralsym | 38.7 | 56.2  | 62.2  | AutoSynRoute | 47.8          | 67.6  | 74.1  | AutoSynRoute | 35.8          |       |       | MEGAN      |
| Molecular similarity   | Molecular Fingerprint | Retrosim  | 37.3 | 54.7  | 63.3  |              |               |       |       |              | 32.8          |       |       | RetroPrime |
| GNN                    | Molecular Graph       | GCN       | 24.9 |       |       |              |               |       |       |              |               |       |       |            |
| GNN                    | Molecular Graph       | GLN       | 52.5 | 69.0  | 75.6  |              |               |       |       |              | 39.3          |       |       | RetroPrime |
| Highway network        | Molecular Fingerprint | - | 44.53 → 44.03 |      |       |              |               |       |       |              |               |       |       |            |
| GCN                    | Molecular Graph       | ChemiRise | 43.8 | 62.1  | 70.1  |              |               |       |       |              |               |       |       |            |
| GNN                    | Molecular Graph       | LocalRetro | 53.4 | 77.5 | 85.9  |              | 54.1          | 73.7  | 79.4  |              |               |       |       |            |
| Transformer(?)         | SMILES(?)             | DualTB    |55.2  | 74.6  | 80.5  |              |               |       |       |              |               |       |       |            |
| Highway network        | Molecular Fingerprint | MHNreact  | 51.8 | 74.6  | 81.2  |              |               |       |       |              |               |       |       |            |
| CNN                    | Molecular Fingerprint + SMILES | multi‑scale feature | 61.1 | 79.1 | 83.9 |             |               |       |       |        |               |       |    |     | 
| GAN                    | Molecular Graph       | RetroComposer | 54.5 | 77.2 | 83.2 |            |               |       |       |              |               |       |       |            |
 

## Reactant-Based Methods 
| Paper                                                        | Year | Journal / Conference         | Code                                                                                 |
| ------------------------------------------------------------ | ---- | ---------------------------- | ------------------------------------------------------------------------------------ |
| Bayesian Algorithm for Retrosynthesis                        | 2020 | JCIM                         | [pytorch](https://github.com/zguo235/bayesian_retro)                                 |
| RetCL: A Selection-based Approach for Retrosynthesis via Contrastive Learning | 2021  |    IJCAI   | [pytorch](https://github.com/hankook/RetCL)                                          |

|Architecture/ Algorithm | Representation | Model   | **USPTO-50K** |       |       | Datasource  | **USPTO-MIT**  |       |       | Datasource  | **USPTO-Full** |       |       | Datasource |
| ---------------------- | -------------- |-------- | ------------- | ----- | ----- | ----------- | -------------- | ----- | ----- | ----------- | -------------- | ----- | ----- | ---------- |
|                        |                |         | **K = 1**     | **3** | **5** |             | **K = 1**      | **3** | **5** |             | **K = 1**      | **3** | **5** |            |
| Bayesian inference + Transformer  | SMILES        | BayesianRetro | 47.5  | 67.2  | 77  |       |                |       |       |             |                |       |       |            |
| GNN + Contrastive Learning | Molecular Graph | RetCL | 71.3       | 86.4  | 92.0  |             |                |       |       |             |                |       |       |            |


## Semi-Template Methods 
| Paper                                                        | Year | Journal / Conference         | Code                                                                                 |
| ------------------------------------------------------------ | ---- | ---------------------------- | ------------------------------------------------------------------------------------ |
| A Graph to Graphs Framework for Retrosynthesis Prediction    | 2020 | ICML                         | [pytorch](https://github.com/DeepGraphLearning/torchdrug)                            |
| RetroXpert: Decompose Retrosynthesis Prediction like a Chemist | 2020 | NIPS                       | [pytorch](https://github.com/uta-smile/RetroXpert)                                   |
| Single-Step Retrosynthesis Prediction Based on the Identification of Potential Disconnection Sites Using Molecular Substructure Fingerprints                                                   |  2021 | JCIM                        | [tensorflow](https://github.com/hasic-haris/one_step_retrosynth_ai)                  |
| Learning Graph Models for Retrosynthesis Prediction          |  2021 | NIPS                        | [pytorch](https://github.com/vsomnath/graphretro)                                    |
| RetroPrime: A Diverse, plausible and Transformer-based method for  Single-Step retrosynthesis predictions | 2021 | Chemical Engineering Journal | [pytorch](https://github.com/wangxr0526/RetroPrime)          |
| G2Retro: Two-Step Graph Generative Models for Retrosynthesis Prediction | 2022 | -                 | [pytorch](https://github.com/ninglab/G2Retro)                                        |
| SemiRetro: Semi-template framework boosts deep retrosynthesis prediction |2022 | ICLR              | -                                                                                    |
| MARS: A Motif-based Autoregressive Model for Retrosynthesis Prediction | 2022 | -                  | -                                                                                    |
| RCsearcher: Reaction Center Identification in Retrosynthesis via Deep Q-Learning | 2023 |     -      | -                                                                                  |
| MechRetro is a chemical-mechanism-driven graph learning framework for interpretable retrosynthesis prediction and pathway planning | 2023 | - |  [pytorch](https://github.com/wangyu-sd/RetroExplainer)   |

|Architecture/ Algorithm | Representation   | Model | **USPTO-50K** |       |       | Datasource  | **USPTO-MIT**  |       |       | Datasource  | **USPTO-Full** |       |       | Datasource |
| ---------------------- | --------------   |------ | ------------- | ----- | ----- | ----------- | -------------- | ----- | ----- | ----------- | -------------- | ----- | ----- | ---------- |
|                        |                  |       | **K = 1**     | **3** | **5** |             | **K = 1**      | **3** | **5** |             | **K = 1**      | **3** | **5** |            |
| GNN                    | Molecular Graph  | G2G   | 48.9          | 67.6  | 72.5  |             |                |       |       |             |                |       |       |            |
| GNN + Transformer      | Molecular Graph + SMILES | RetroXpert | 50.4     | 61.1  | 62.3   | GraphRetro    |     |       |       |             |                |       |       |            |
| Highway network        | Molecular Fingerprint    | MolecularSub FP | 47.2 | 55.7 | 61.5 |      |                |       |       |             | 44.4           |       |       | MEGAN      |
| GNN                    | Molecular Graph  | GraphRetro | 53.7     | 68.3  | 72.2  |             |                |       |       |             |                |       |       |            |
| Transformer            | SMILES           | RetroPrime | 51.4     | 70.8  | 74    |             |                |       |       |             | 44.1           |       |       |            |
| GNN                    | Molecular Graph  | G2Retro | 54.1        | 74.1  | 81.2  |             |                |       |       |             |                |       |       |            |
| GNN                    | Molecular Graph  | SemiRetro | 54.9      | 75.3  | 80.4  |             |                |       |       |             |                |       |       |            |
| GNN + Transformer      | Molecular Graph  | MARS  | 54.6          | 76.4  | 83.3  |             |                |       |       |             |                |       |       |            | 
| GNN + RL               | Molecular Graph  | RCsearcher | -        | -     | -     |             |                |       |       |             |                |       |       |            |
| Graphormer             | Molecular Graph  | MechRetro  | 58.0     | 73.5  | 77.2  |             |                |       |       |             |                |       |       |            |

## Template-Free Generation Methods 
| Paper                                                        | Year | Journal / Conference         | Code                                                                                 | 
| ------------------------------------------------------------ | ---- | ---------------------------- | ------------------------------------------------------------------------------------ |
| Retrosynthetic Reaction Prediction Using Neural Sequence to Sequence Models    | 2017 | ACS Central Science | [tensorflow](https://github.com/pandegroup/reaction_prediction_seq2seq)     |
| A Transformer Model for Retrosynthesis                                        | 2019 | ICANN               | [tensorflow](https://github.com/bigchem/retrosynthesis)                      |
| Retrosynthesis with Attention-Based NMT Model and Chemical Analysis of the "Wrong" Predictions | 2019 | RSC Advance | [tensorflow](https://github.com/hongliangduan/ )                    |
| Predicting Retrosynthetic Reactions Using Self-Corrected Transformer Neural Networks | 2020 | JCIM         | [pytorch](https://github.com/yuedongyang/SCROP)                              |
| Automatic Retrosynthetic Route Planning Using Template-Free Models            | 2020 | Chemical Science    | [tensorflow](https://github.com/PKUMDL-AI/AutoSynRoute)                      |
| State-of-the-art augmented NLP transformer models for direct and single-step retrosynthesis | 2020 | Nature Communications | [tensorflow](https://github.com/bigchem/synthesis)           |
| GTA: Graph Truncated Attention for Retrosynthesis            | 2021 | AAAI                                 | [pytorch](https://github.com/sw32-seo/GTA)                                   |
| Valid, Plausible, and Diverse Retrosynthesis Using Tied Two-way Transformers with Latent Variables | 2021 | JCIM         | [pytorch](https://github.com/ejklike/tied-twoway-transformer/) |
| Molecular graph enhanced transformer for retrosynthesis prediction | 2021 | Neurocomputing                 | [pytorch](https://github.com/papercodekl/MolecularGET)                       |
| Molecule Edit Graph Attention Network: Modeling Chemical Reactions as Sequences of Graph Edits | 2021 | JCIM | [pytorch+tensorflow](https://github.com/molecule-one/megan)                |
| Retrosynthesis prediction using grammar-based neural machine translation: An information-theoretic approach | 2021 | Computers and Chemical Engineering | [tensorflow](https://github.com/vupil/grammarTransformerReactionPrediction) |
| Substructure-based neural machine  translation for retrosynthetic prediction | 2021 | Journal of Cheminformatics | [pytorch](https://github.com/knu-chem-lcbc/fragment_based_retrosynthesis) |
| Towards understanding retrosynthesis by energy-based models   | 2021 | NIPS                                 | -                                                                           |
| Chemformer: A Pre-Trained Transformer for Computational Chemistry | 2022 | Machine Learning: Science and Technology | [pytorch](https://github.com/MolecularAI/Chemformer)                |
| Retrosynthetic reaction pathway prediction through neural machine translation of atomic environments | 2022 | Nature Communications | [pytorch](https://github.com/knu-lcbc/RetroTRAE)             |
| Root-aligned SMILES: A Tight Representation for Chemical Reaction Prediction | 2022 |  Chemical Science |                          [pytorch](https://github.com/otori-bird/retrosynthesis)|
| Permutation Invariant Graph-to-Sequence Model for Template-Free Retrosynthesis and Reaction Prediction | 2022 |  JCIM |             [pytorch](https://github.com/coleygroup/Graph2SMILES)|
| Unified Deep Learning Model for Multitask Reaction Predictions with Explanation | 2022 |  JCIM                          |             [pytorch](https://github.com/HelloJocelynLu/t5chem) |
| Modeling Diverse Chemical Reactions for Single-step Retrosynthesis via Discrete Latent Variables | 2022 | CIKM |    -                                                                     |
| G2GT: Retrosynthesis Prediction with Graph to Graph Attention Neural Network and Self-Training | 2022 | JCIM | [pytorch](https://github.com/Anonnoname/G2GT_2)                            |
| Retroformer: Pushing the Limits of End-to-end Retrosynthesis Transformer | 2022 | JCML | [pytorch](https://github.com/yuewan2/Retroformer)                                                |
| Single-step retrosynthesis prediction by leveraging commonly preserved substructures | 2023 | Nature Communications | [link](https://github.com/fangleigit/RetroSub) |


|Architecture/ Algorithm | Representation | Model   | **USPTO-50K** |       |       | Datasource   | **USPTO-MIT**  |       |       | Datasource  | **USPTO-Full** |       |       | Datasource |
| ---------------------- | -------------- |-------- | ------------- | ----- | ----- | ------------ | -------------- | ----- | ----- | ----------- | -------------- | ----- | ----- | ---------- |
|                        |                |         | **K = 1**     | **3** | **5** |              | **K = 1**      | **3** | **5** |             | **K = 1**      | **3** | **5** |            |
| LSTM                   | SMILES         | seq2seq | 28.3          | 42.8  | 47.3  | AutoSynRoute | 46.9           | 61.6  | 66.3  | AutoSynRoute |               |       |       |            |
| Transformer            | SMILES         | Transformer | 42.7      | 63.9  | 69.8  |              | 53.8           | 70.5  | 75.3  | a            | 44.7          | 61.1  |  66.0 | a          |
| Transformer            | SMILES         | T2T     | -             | -     | -     |              | -              | -     | -     |              |               |       |       |            |
| Transformer            | SMILES         | SCROP   | 43.7          | 60.0  | 65.2  |              |                |       |       |              | 41.5          | 53.3  | 56.7  |            |
| Transformer            | SMILES         | AutoSynRoute | 43.1     | 64.6  | 71.8  |              | 54.1           | 71.8  | 76.9  |              |               |               |            |
| Transformer            | SMILES         | AT(X=100) | 53.5         | 69.4  | 81.0 |              |                |       |       |              | 46.2          |       |       | RetroPrime |
| Transformer            | SMILES         | GTA     | 51.1          | 67.6  | 74.8  |              |                |       |       |              | 46.6          |       |       |            |
| Transformer            | SMILES         | Tied Two-way Transformer | 47.1 | 67.1  |73.1          |                |       |       |              |               |       |       |            |
| Transformer            | SMILES + Molecular Graph | MolecularGET | 44.9 | 58.8 | 62.4            |                |       |       |              |               |       |       |            |
| GNN                    | Molecular Graph | MEGAN   | 48.1         | 70.7  | 78.4  |              |                |       |       |              | 33.6          |       |       |            |
| Transformer            | Customized String | Grammar Transformer | 32.1   | 44.3 | 48.9          |                |       |       |              |               |       |       |            |
| Transformer            | Customized String | Fragment-based Transformer | 29 |    |              |                |       |       |              |               |       |       |            |
| Transformer            | SMILES         | DualTF   | 53.6         | 70.7  | 74.6  |              |                |       |       |              |               |       |       |            |
| Transformer            | SMILES         | Chemformer | 54.3       |       |  62.3 |              |                |       |       |              |               |       |       |            |
| Transformer            | Customized String | RetroTRAE |          |       |       |              | 58.3           | 66.1  | 69.4  |              |               |       |       |            |
| Transformer            | SMILES         | Root-aligned SMILES | 56.3 | 79.2 | 86.2  |            | 60.3           | 78.2  | 83.2  |              | 48.9          | 66.6  | 72.0  |            |
| Transformer + GNN      | SMILES + Molecular Graph | Graph2SMILES | 52.9 | 66.5 | 70.0  |         |                |       |       |              | 45.7          |       |       |            |
| Transformer            | SMILES         | T5Chem  | 46.5          | 64.4  | 70.5  |              |                |       |       |              |               |       |       |            |
| Transformer + variational autoencoders | SMILES |  RetroDCVAE     | 53.1  | 68.1 | 71.6 |        |                |       |       |              |               |       |       |            |
| Graphormer             | Molecular Graph | G2GT  | 54.1           | 69.9  | 74.5  |              |                |       |       |              | 49.3          | 60.0  |  68.9 |            |
| Graph Transformer      | Molecular Graph       | Retroformer      | 53.2  | 71.1  | 76.6         |                |       |       |              |               |       |       |            |
| Transformer            | Customized String | RetroSub |           |       |       |              |                |       |       |              | 53.6          |       |            |


## Witting for update
| Paper                                                        | Year | Journal / Conference         | Code                                                                                 | 
| ------------------------------------------------------------ | ---- | ---------------------------- | ------------------------------------------------------------------------------------ |
| Learning to Make Generalizable and Diverse Predictions for Retrosynthesis   | 2019 | ICML             | -                                                                                 |
| Molecular Transformer unifies reaction prediction and retrosynthesis across pharma chemical space | 2019 | chem comm | [pytorch](https://github.com/pschwllr/MolecularTransformer)        |
| Data Transfer Approaches to Improve Seq-to-Seq Retrosynthesis | 2020 | ICLR                        | -                                                                                    |
| Dual-view Molecule Pre-training | 2021 | NeurIPS | [pytorch](https://github.com/microsoft/DVMP) and [pytorch](https://github.com/dual-view-molecule-pretraining/dmp)                     |

|Architecture/ Algorithm | Representation | Model   | **USPTO-50K** |       |       | Datasource   | **USPTO-MIT**  |       |       | Datasource  | **USPTO-Full** |       |       | Datasource |
| ---------------------- | -------------- |-------- | ------------- | ----- | ----- | ------------ | -------------- | ----- | ----- | ----------- | -------------- | ----- | ----- | ---------- |
|                        |                |         | **K = 1**     | **3** | **5** |              | **K = 1**      | **3** | **5** |             | **K = 1**      | **3** | **5** |            |
| Transformer            | SMILES         | LV-Trans | 44.8         | 64.9  | 72.4  |              |                |       |       |              |               |       |       |            |
| Transformer            | SMILES(?)      | Molecular Transformer | 43.8 |  | 60.5  |              |                |       |       |              |               |       |       |            |
| Transformer            | SMILES(?)      |  pre-training plus fine-tuning | 57.4 | 77.6 | 83.1 |      |            |       |       |              |               |       |       |            |
| Transformer + GNN      | SMILES + Molecular Graph | DMP - transformer | 46.1 | 65.2 | 70.4 |     |            |       |       |                  |       45.0    |  59.6 | 63.9  |            |
| Transformer + GNN      | SMILES +Molecular Graph  | DMP -GNN      | 54.2  | 70.5  | 77.2         |                |       |       |              |               |       |       |            |
