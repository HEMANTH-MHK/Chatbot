# IntentBot 
Real-Time Chatbot with Intent Classification

## Table of Contents
+ [About](#about)
+ [Requirements](#installing)
    + [Environment](#env)
    + [Python Requirements](#pyinstalling)
+ [Running the code](#run)
    + [Chatbot-Intent-Classification](#run-classification)
    + [Chatbot-Interaction](#run-interaction)
+ [Output](#out)
+ [Result](#result)

## About <a name = "about"></a>

This project demonstrates a complete pipeline for creating a chatbot that understands and responds to user inputs based on predefined intents.It includes two main components:

- Chatbot-Intent-Classification: Trains a neural network model using TensorFlow/Keras to classify user input into intents based on patterns in the input data.

- Chatbot-Interaction: Allows real-time interaction with the trained chatbot. The system predicts the intent of user input and responds accordingly using predefined responses from the intents.json file.

## Requirements <a name = "installing"></a>

This project has been tested on Ubuntu 20.04.

## Environment <a name = "env"></a>

The project was implemented in a Python environment utilizing TensorFlow for deep learning, scikit-learn for encoding labels, and Colorama for colored console output.

### Python Requirements <a name = "pyinstalling"></a>

1. Create a new virtual environment using conda:
    ```ShellSession
    conda create -n chatbotenv
    conda activate chatbotenv
    ```
    
2. Install the required python packages
    ```ShellSession
    pip install numpy tensorflow scikit-learn colorama
    ```
    
## Running the code <a name = "run"></a>
## Chatbot-Intent-Classification <a name = "run-classification"></a>

This component trains the model using the data in intents.json.
Ensure the intents.json file is in the working directory. This file contains the intents, patterns, and responses used for training.

Run the training script to create the model:
```ShellSession
$ conda activate chatbotenv
$ python3 chatbot_intent_classification.py
```
**What the script does:**

- Loads the intents from the intents.json file.
- Prepares training data by tokenizing patterns and encoding labels.
- Defines a Sequential model using embedding and dense layers.
- Trains the model for 500 epochs and saves the trained model, tokenizer, and label encoder for 
  future use.

## Chatbot-Interaction <a name = "run-interaction"></a>
Once the model is trained, this component enables interactive chat with the bot.
Ensure the files chat_model.keras, tokenizer.pickle, and label_encoder.pickle are in the working directory.

Run the interaction script:
```ShellSession
$ conda activate chatbotenv
$ python3 chatbot_interaction.py
```
**What the script does:**

- Loads the pre-trained model, tokenizer, and label encoder.
- Starts a chat session where the bot predicts intents based on user input and responds with predefined responses.
- Type "quit" to exit the chat.
## Output <a name = "out"></a>
**Chatbot-Intent-Classification Output:**
- Displays the training progress, including the loss and accuracy of the model over epochs.
- Saves the model and associated objects (chat_model.keras, tokenizer.pickle, and label_encoder.pickle).

**Chatbot-Interaction Output:**
- The bot starts a chat session, recognizing and responding to user inputs with appropriate answers.
- User inputs are displayed in light blue, and bot responses in green, providing a clear, color-coded interaction.
## Result <a name = "result"></a>
**Chatbot-Intent-Classification:** Successfully trains a model that classifies user inputs into intents using the neural network, demonstrating effective learning from the provided data.

**Chatbot-Interaction:** The bot accurately interprets inputs and engages in meaningful conversations based on the detected intent, showcasing a practical application of the intent classification model in a real-time setting.



![image](https://github.com/user-attachments/assets/e6b77ab0-a500-487f-b50e-e38cea115882)
