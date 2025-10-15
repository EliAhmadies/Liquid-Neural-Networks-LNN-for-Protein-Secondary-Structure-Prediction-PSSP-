# Liquid Neural Networks (LNN) for Protein Secondary Structure Prediction (PSSP)

## Project Overview

This repository contains the implementation of **Liquid Time-Constant (LTC) Networks**, a class of novel, highly expressive time-continuous Recurrent Neural Networks (RNNs), applied to the task of **Protein Secondary Structure Prediction (PSSP)**.

The project explores how these brain-inspired, ODE-based networks perform in predicting the structural hierarchy of proteins (Helix, Sheet, Coil) from their primary amino acid sequence. We compare the performance of LTCs against traditional RNN architectures (LSTM, CTGRU, CTRNN) and investigate the impact of various input representations, including classic one-hot vectors and developed physical feature encodings (NNI and NNIH).

## Key Features

* **LTC Network Implementation:** A TensorFlow/Keras implementation of the Liquid Time-Constant (LTC) Recurrent Cell. The network uses a hidden state equation based on a differential equation.

* **PSSP Methodology:** Implementation of the full pipeline for protein sequence processing and secondary structure prediction.

* **Feature Engineering:** Development and testing of custom input representations:

  * **NNI (Neighbour-Neighbour Interaction):** Interaction score based purely on amino acid proximity within a defined window.

  * **NNIH (NNI with Hydrophobicity):** Augments the NNI score with hydrophobicity properties of the amino acids.

* **Hyperparameter Search:** Extensive GridSearch experiments to identify optimal hyperparameters (Learning Rate, Optimizer, Activation Function, Window Size) for the LTC model.

## Datasets

The models were trained and tested on several benchmark protein structure datasets. *Note: Data files are not included in this repository and must be acquired separately.*

| Dataset Name | Number of Proteins | Sequence Length Range | Test Accuracy (+/-) | 
 | ----- | ----- | ----- | ----- | 
| **CB513** | 514 | 20 - 874 | $0.56 \pm 0.01$ | 
| **CASP12** | 21 | 76 - 1494 | $0.64 \pm 0.01$ | 
| **PDB (Subset)** | 9079 | 20 - 1632 | $0.59 \pm 0.01$ | 
| **CATH40** | 31731 | 18 - 497 | $0.64 \pm 0.01$ | 

The data is expected to be in a processed **JSON format**, containing amino acid sequences and corresponding DSSP-classified secondary structure labels.

## Installation and Setup

### Prerequisites

* Python 3.8+

* NVIDIA GPU (Recommended for training large models on CATH40)

### Clone the Repository

```bash
git clone https://github.com/EliAhmadies/Liquid-Neural-Networks-LNN-for-Protein-Secondary-Structure-Prediction-PSSP-.git
cd LNN-PSSP
```

### Install Dependencies

We recommend using a virtual environment.

```bash
python -m venv venv
source venv/bin/activate  # On Linux/macOS

.\venv\Scripts\activate # On Windows
pip install -r requirements.txt
```

## Usage

### 1. Data Preparation

Place your processed JSON data files (e.g., `cath40_data.json`) into a `/data` directory.

### 2. Training the LTC Model

To train the LTC model using the optimal settings found during the GridSearch (Adam optimizer, LR: 0.05, Sigmoid activation), run the main script:

I understand. You want the entire content of the currently open document, file_content.txt, presented inside a single, continuous code block.

Here is the content, wrapped as requested:

# Liquid Neural Networks (LNN) for Protein Secondary Structure Prediction (PSSP)

## Project Overview

This repository contains the implementation of **Liquid Time-Constant (LTC) Networks**, a class of novel, highly expressive time-continuous Recurrent Neural Networks (RNNs), applied to the task of **Protein Secondary Structure Prediction (PSSP)**.

The project explores how these brain-inspired, ODE-based networks perform in predicting the structural hierarchy of proteins (Helix, Sheet, Coil) from their primary amino acid sequence. We compare the performance of LTCs against traditional RNN architectures (LSTM, CTGRU, CTRNN) and investigate the impact of various input representations, including classic one-hot vectors and developed physical feature encodings (NNI and NNIH).

## Key Features

* **LTC Network Implementation:** A TensorFlow/Keras implementation of the Liquid Time-Constant (LTC) Recurrent Cell. The network uses a hidden state equation based on a differential equation.

* **PSSP Methodology:** Implementation of the full pipeline for protein sequence processing and secondary structure prediction.

* **Feature Engineering:** Development and testing of custom input representations:

  * **NNI (Neighbour-Neighbour Interaction):** Interaction score based purely on amino acid proximity within a defined window.

  * **NNIH (NNI with Hydrophobicity):** Augments the NNI score with hydrophobicity properties of the amino acids.

* **Hyperparameter Search:** Extensive GridSearch experiments to identify optimal hyperparameters (Learning Rate, Optimizer, Activation Function, Window Size) for the LTC model.

## Datasets

The models were trained and tested on several benchmark protein structure datasets. *Note: Data files are not included in this repository and must be acquired separately.*

| Dataset Name | Number of Proteins | Sequence Length Range | Test Accuracy (+/-) | 
 | ----- | ----- | ----- | ----- | 
| **CB513** | 514 | 20 - 874 | $0.56 \pm 0.01$ | 
| **CASP12** | 21 | 76 - 1494 | $0.64 \pm 0.01$ | 
| **PDB (Subset)** | 9079 | 20 - 1632 | $0.59 \pm 0.01$ | 
| **CATH40** | 31731 | 18 - 497 | $0.64 \pm 0.01$ | 

The data is expected to be in a processed **JSON format**, containing amino acid sequences and corresponding DSSP-classified secondary structure labels.

## Citation

If you use this code or methodology in your research, please cite the original works on Liquid Time-Constant Networks:

* Mathias Lechner et al. (2020) - *Liquid Time-Constant Networks*

* Hasani et al. (2020) - *Liquid Time-Constant Networks for Real-Time Processing*

## Contact

For questions or collaborations, please open an issue or contact the contributors:
* Ahmadieslamloo Elaheh
* Ausilio Lorenzo
* Jafarpour Farshad
* Prodan George
