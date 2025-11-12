# Next-Word Generation using RNN

# A deep learning project that demonstrates next-word prediction and text generation using a Recurrent Neural Network (LSTM). This project is ideal for learning about sequence modeling, NLP, and hands-on deep learning workflows.

#Key Features

Preprocess and tokenize raw text to build a vocabulary.

Convert text into sequences suitable for RNN training.

Train an LSTM-based language model to predict the next word in a sequence.

Save and load model checkpoints for reuse.

Generate new text using greedy or top-k sampling with temperature control.

Evaluate model performance using loss and perplexity metrics.

# Repository Structure
data/          → raw and processed text data
src/           → model definition, training scripts, and generation scripts
checkpoints/   → saved model checkpoints
notebooks/     → experiments, visualizations, and examples

# How to Use

Install dependencies

pip install -r requirements.txt


Preprocess your data

python src/data.py --input data/raw/train.txt


Train the model

python src/train.py --epochs 10 --batch_size 64


Generate text

python src/generate.py --checkpoint checkpoints/model.pt --seed "Once upon a time"

# Model Overview

Architecture: Embedding → LSTM → Linear layer

Hyperparameters:

hidden size: 256–512

layers: 1–3

dropout: 0.2–0.5

learning rate: 1e-3

Designed to handle variable-length sequences efficiently.

# Evaluation

Monitors training and validation loss.

Computes perplexity to measure prediction quality.

Optional: top-k accuracy or word-level accuracy on validation set.

# License

MIT License — free for personal, educational, or research purposes.
