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
The model is implemented in Python and utilizes popular libraries such as NumPy and Matplotlib for data manipulation and visualization. Users can input their dataset, specify the model parameters, and run comprehensive genetic epidemiological analyses with ease.

### 1. Clone the repository:

 ```bash
git clone https://github.com/yourusername/GENet.git
cd GENet
```

### 2. Install the required packages

!pip install -r requirements.txt

### 3. Run the provided notebook:
Upload the GEnet (1).ipynb file to your Google Colab environment and open it. Run the cells sequentially to execute the code.

## Usage Examples
Here are some basic steps to get started with GENet:

1. Load your dataset:
Adjust the code in the notebook to load your dataset as required.

2. Train the model:
Follow the steps in the notebook to train the model on your data.

3. Predict and visualize:
Use the trained model to make predictions and visualize the results.

## Contributions
Contributions are welcome! If you have suggestions for improvements or new features, please feel free to fork the repository and submit a pull request.

## License
This project is licensed under the MIT License - see the LICENSE file for details.
