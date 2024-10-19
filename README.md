
# Language Translator (English to French Case Study) Bag of Characters Encoder-Decoder Model


This project is a character-level sequence-to-sequence model for translating English to French. The model is built using TensorFlow and Keras, leveraging LSTM layers for the encoder-decoder architecture. The project also includes a Tkinter-based graphical user interface (GUI) to interact with the model and translate text in real-time.

## Overview

The project consists of an English-to-French language translator using the following key components:
- **Data Preprocessing**: Prepares the text data by tokenizing and vectorizing the input and target texts.
- **Model Architecture**: Implements a sequence-to-sequence LSTM model with attention mechanism to handle character-level translation.
- **GUI**: A simple Tkinter-based interface for inputting English sentences and receiving translated French sentences.


## Features

- Character-level tokenization using `CountVectorizer`.
- Padding of input and target sequences to match the required length for training.
- Encoder-Decoder architecture using LSTM layers.
- Model training with `categorical_crossentropy` loss and `adam` optimizer.

## Installation

To get started, you need to set up your environment with the necessary dependencies.

1. Clone this repository to your local machine:
   ```bash
   git clone https://github.com/Olamide643/Language-Translator.git
   ```
2. Navigate to the project directory:
   ```bash
   cd language-translator
   ```

To run this project, you will need:

- Python 3.x
- The following libraries:
  - `numpy`
  - `tensorflow`
  - `scikit-learn`

You can install the dependencies using:

```bash
pip install numpy tensorflow scikit-learn
```




## Usage

1. **Data Preparation**: Make sure to provide a dataset in the format of a tab-separated file containing English-French sentence pairs. Modify the `data_path` variable in the script to point to your dataset (`fra.txt` by default).

2. **Model Training**:
   To train the model, run the following command:
   ```bash
   python train.py
   ```
   This script preprocesses the data, trains the model using LSTM layers, and saves the trained model and tokenizer to disk.

3. **Running the GUI**:
   Once the model is trained, you can start the Tkinter GUI by running:
   ```bash
   python gui.py
   ```
   Enter an English sentence into the provided text box, and the model will return the corresponding French translation.


### Example

```python
# Sample input data (input_texts and target_texts need to be prepared)
input_texts = ['hello', 'world']
target_texts = ['hola', 'mundo']

# Call the function to prepare data
en_in_data, dec_in_data, dec_tr_data = bagofcharacters(input_texts, target_texts)

# Train the model
model.fit([en_in_data, dec_in_data], dec_tr_data, batch_size=64, epochs=100, validation_split=0.2)
```

## Contributing

If you'd like to contribute to this project, feel free to fork the repository and submit a pull request.


## Sample 

<p align="center">
  <img src="/Sample.png" width="700" title="hover text">
</p>

