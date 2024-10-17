
# Bag of Characters Encoder-Decoder Model

This repository contains an implementation of an encoder-decoder model for sequence-to-sequence learning using a "Bag of Characters" approach. The model is designed to tokenize input text at the character level and process it for tasks such as text generation or machine translation.

## Overview

The core functionality of this code revolves around tokenizing text data into individual characters and preparing it for an encoder-decoder model using LSTM (Long Short-Term Memory) networks. The model is trained using `categorical_crossentropy` loss and is designed to map input character sequences to output sequences.

## Features

- Character-level tokenization using `CountVectorizer`.
- Padding of input and target sequences to match the required length for training.
- Encoder-Decoder architecture using LSTM layers.
- Model training with `categorical_crossentropy` loss and `adam` optimizer.

## Installation

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

1. **Input Data Preparation:**
   The function `bagofcharacters` takes `input_texts` and `target_texts` as inputs, tokenizes the text at the character level using `CountVectorizer`, and pads the sequences as necessary.

2. **Model Architecture:**
   - An LSTM-based encoder takes the input sequences.
   - The decoder is also an LSTM that uses the encoder's states to generate target sequences.
   - The model outputs sequences using a softmax activation layer.

3. **Training:**
   After defining the model, it is compiled using the `adam` optimizer and trained with `categorical_crossentropy` as the loss function and `accuracy` as a metric.

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

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Sample 

<p align="center">
  <img src="/sample.png" width="700" title="hover text">
</p>

