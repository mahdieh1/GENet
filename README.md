# GENet

## Overview
GENet (Gene Expression Network from Histone and TF Integration) is a novel supervised model architecture designed to predict gene expression. This architecture effectively combines Graph Convolutional Networks (GCNs) with a unique integration approach to enhance the prediction of gene expression levels.

![image](https://github.com/mahdieh1/GENet/assets/12238056/050172e2-ed16-473e-a9d7-04d41ec714b6)


## Model Architecture
Initially, GENet employs Graph Convolutional Networks (GCNs) to tackle the classification task for each feature. We construct a weighted sample similarity network for each feature type using cosine similarity, which serves as the input for the GCNs. The strength of GCNs lies in their capability to utilize both attribute data and sample interconnections, thereby enhancing prediction accuracy.

Each GCN receives these similarity networks as inputs and is trained to produce preliminary class label predictions. Subsequently, these initial predictions from each feature-specific GCN are used to assemble a cross-feature discovery tensor. This tensor identifies correlations between labels across different features and is transformed into a vector. This vector is then applied to a regression model to make the final label predictions.

## Workflow Description
The workflow of GENet involves several crucial steps:

Feature Matrix Construction: Each feature data type is represented as a matrix, where shades of blue and purple indicate data intensities or values.
Sample Similarity Network Formation: These matrices are utilized to construct sample similarity networks, depicted as interconnected nodes.
GCN Processing: Separate GCNs process these networks to capture complex data relationships, outputting initial predictions.
Integration into Final Prediction Model: These predictions are fed into the Correlation Discovery Network, which merges the information to generate a final predictive output visualized as vertically aligned gray bars indicating the predicted classes or outcomes.

## Getting Started

To get started with GENet, clone the repository and navigate to the installation directory:
## Running Google Colab

### 1. Clone the repository:

!git clone https://github.com/mahdieh1/GENet.git
%cd GENet

### 2. Install the required packages

!pip install numpy pandas seaborn matplotlib scipy scikit-learn torch

### 3. Run the provided notebook:

After cloning the repository and installing the packages, you can run the cells in the GENet.ipynb notebook.

## Running on notebook

### 1. Clone the repository:

 ```bash
git clone https://github.com/mahdieh1/GENet.git
cd GENet
```

### 2. Install the required packages

pip install numpy pandas seaborn matplotlib scipy scikit-learn torch

### 3. Run the provided notebook:

jupyter nbconvert --to notebook --execute GENet.ipynb



## Usage Examples
You can run the provided example by opening example.ipynb in Google Colab or Jupyter Notebook and running all the cells. This notebook demonstrates how to generate example data, construct similarity networks, train the GCN model, and perform regression.

### Defining User Input for the Model
To define their input for the model, users need to provide input files in a specific format. Below are the details of the input and output formats:

#### Input Format
Cell Line Data:
The input files should contain data for various cell lines. Each file should be a tab-separated values (TSV) file.

#### Target Values:
A separate file should contain the target values. This file should have a single column with the target values corresponding to each cell line.

## Contributions
Contributions are welcome! If you have suggestions for improvements or new features, please feel free to fork the repository and submit a pull request.

## License
This project is licensed under the MIT License - see the LICENSE file for details.
