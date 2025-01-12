# Name Classification with a Character-Level RNN

This project demonstrates how to build and train a Recurrent Neural Network (RNN) to classify names into their language of origin based on their spelling. The implementation uses PyTorch and covers data preparation, model training, evaluation, and prediction.

## Features

- **Data Preparation**: Names from 18 languages are processed and converted into a format suitable for machine learning.
- **Tensor Conversion**: Names are encoded using one-hot vectors.
- **RNN Architecture**: A simple RNN with two linear layers and a LogSoftmax activation is implemented.
- **Training Pipeline**: Includes loss calculation, backpropagation, and loss tracking.
- **Evaluation**: Provides confusion matrices and loss plots for analysis.
- **User Input Predictions**: Predicts the language of names entered by the user.

## Dataset

The dataset consists of 18 text files, each representing a language. Each file contains a list of names, one per line. Download the dataset [here](https://download.pytorch.org/tutorial/data.zip) and extract it to the `data/names/` directory.

## Installation

1. Clone the repository.
2. Install the required libraries:
    ```bash
    pip install torch matplotlib
    ```
3. Ensure the dataset is available in the `data/names/` directory.

## Usage

### Training the Model

Run the notebook to preprocess the data, define the RNN, and train it. Training involves the following steps:

1. Converting names to tensors.
2. Feeding names into the RNN, letter by letter.
3. Calculating loss using `nn.NLLLoss`.
4. Updating model weights using backpropagation.

### Evaluation

- Visualize training progress with loss plots.
- Analyze the confusion matrix to identify classification patterns and errors.

### Making Predictions

Use the `predict` function to classify user-provided names:
```python
predict('Smith')
predict('Hernandez')
predict('Tanaka')
