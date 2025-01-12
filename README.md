Name Classification with a Character-Level RNN

This project demonstrates how to build and train a Recurrent Neural Network (RNN) to classify names into their language of origin based on their spelling. The implementation uses PyTorch and covers data preparation, model training, evaluation, and prediction.

Features

Data Preparation: Names from 18 languages are processed and converted into a format suitable for machine learning.

Tensor Conversion: Names are encoded using one-hot vectors.

RNN Architecture: A simple RNN with two linear layers and a LogSoftmax activation is implemented.

Training Pipeline: Includes loss calculation, backpropagation, and loss tracking.

Evaluation: Provides confusion matrices and loss plots for analysis.

User Input Predictions: Predicts the language of names entered by the user.

Dataset

The dataset consists of 18 text files, each representing a language. Each file contains a list of names, one per line. Download the dataset here and extract it to the data/names/ directory.

Installation

Clone the repository.

Install the required libraries:

pip install torch matplotlib

Ensure the dataset is available in the data/names/ directory.

Usage

Training the Model

Run the notebook to preprocess the data, define the RNN, and train it. Training involves the following steps:

Converting names to tensors.

Feeding names into the RNN, letter by letter.

Calculating loss using nn.NLLLoss.

Updating model weights using backpropagation.

Evaluation

Visualize training progress with loss plots.

Analyze the confusion matrix to identify classification patterns and errors.

Making Predictions

Use the predict function to classify user-provided names:

predict('Smith')
predict('Hernandez')
predict('Tanaka')

Key Functions

findFiles(pattern): Locates files matching a given pattern.

letterToIndex(letter): Converts a letter to its index in the alphabet.

train(category_tensor, line_tensor): Trains the RNN on a single example.

predict(input_line, n_predictions=3): Predicts the top N languages for a given name.

Libraries Used

PyTorch (torch, torch.nn)

Data manipulation (os, unicodedata, string, glob, random)

Visualization (matplotlib)

Results

Loss Plot: Displays the decrease in loss over training iterations.

Confusion Matrix: Shows the accuracy of predictions for each language.
