# JuniorGPT: A GPT Implementation for Shakespeare Dataset
JuniorGPT is a light implementation of the GPT (Generative Pre-trained Transformer) model focused on generating text in the style of Shakespeare. This repository contains code to train a model using a subset of Shakespeare's works and subsequently generate text resembling the bard's style.

# Project Overview
JuniorGPT is designed to:
1. Load Shakespeare text data.
2. Tokenize the data and create a vocabulary.
3. Define and initialize a GPT-like architecture.
4. Train the model.
5. Generate Shakespearean-style text.

# System Requirements
- Python 3.x
- PyTorch (latest version)
- CUDA (if using GPU for training)

# Setup and Run
1. Place your Shakespeare dataset named input.txt in the root directory.
2. Run the script. The script will train the model and generate text samples.
3. Find the generated Shakespearean-style text in the output.txt file.

# Code Structure
- Initial Setup: Hyperparameters, GPU check, manual seed, and other configuration details.
- Data Preparation:
  - Loading the Shakespeare dataset.
  - Tokenizing the text and creating a vocabulary for unique characters.
  - Splitting the data into training and validation sets.
- Model Architecture:
  - Definition of various sub-modules (like MultiHeadAttention, FeedFoward, and Block) which will be used in the main GPT model.
  - Main GPT model (called GPTLanguageModel) defined using the sub-modules.
- Training Loop:
  - The model is trained using the AdamW optimizer.
  - Loss is estimated every eval_interval steps.
- Text Generation:
  - A context tensor is initialized with zeros.
  - The model generates text in the style of Shakespeare. This text is saved to output.txt.

# Output
At the end of the training, you will see a sample output printed in the console. Additionally, the generated text will be saved in output.txt in the root directory.
