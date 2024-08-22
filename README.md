# DeepChess
Neural Network architecture able to learn position evaluation from scratch. This project draws inspiration from the 2016 paper ["DeepChess: End-to-End Deep Neural Network
for Automatic Learning in Chess"](https://www.cs.tau.ac.il/~wolf/papers/deepchess.pdf).


**Project Description:**
This project focuses on building a deep learning model to analyze and evaluate chess positions. The model uses an autoencoder architecture to learn representations of chessboard states, allowing it to distinguish between winning and losing positions. The project involves curating a dataset of chess positions, loading them into dataloaders, and implementing the necessary neural network architecture.

**How It Works:**
- **Data Preparation:** Chess positions are loaded from a curated dataset into dataloaders, where the data is shuffled to ensure diversity in training. The positions are prepared to match the required input size for the model.
- **Model Architecture:** The project implements an autoencoder using PyTorch. This architecture is designed to encode chessboard states into a lower-dimensional space and then decode them back, ensuring that the network captures essential features of the positions.
- **Training & Evaluation:** The model is trained to minimize reconstruction error, with separate functions for training and evaluation. The training process iterates through the dataset, optimizing the model weights.

**How to Run:**
1. **Environment Setup:** Ensure that you have the required libraries installed, including `torch`, `numpy`, `matplotlib`, and `chess`. You can install these via pip:
   ```bash
   pip install torch numpy matplotlib python-chess tqdm
   ```
2. **Data Download:** The project includes commands to automatically download the necessary dataset and pre-trained model weights. These can be downloaded by running the following commands within the notebook:
   ```python
   !gdown --id 1GCR9xVlIKXa0v-Q6XCbWPNDGkA6JRyAL
   !gdown --id 1diprHGEiViYrm7KFbRCxClq90T3iKp3I
   !gdown --id 19MnhZkDMqOz3Tw1oOmvvm3DeuLqGqMmQ
   !gdown --id 1JUAr_ljsmgOq8edVCQm43KxERQpSGd75
   ```
3. **Running the Model:** Load the dataset and initiate training by running the cells in the Jupyter notebook. The code includes visualization tools and evaluation functions to monitor model performance.


This repository is part of the Deep Learning course given by Jian Tang at H.E.C Montréal 
