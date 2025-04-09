# Python AI Chatbot

This AI chatbot is built using TensorFlow and TFLearn. It's designed to process intents from a JSON file, preprocess the data, create a bag-of-words representation, construct a neural network, train the model, and finally utilize the trained model to respond to user input based on the detected intent.".
<br />
<br />
This is a simplified chatbot, and more sophisticated chatbots might involve a combination of natural language understanding (NLU) and natural language generation (NLG) systems, as well as the use of pre-trained language models like GPT-3 for more human-like interactions.

## How This Code Works

### 1. Importing Libraries:

The code begins by importing the necessary libraries, including NumPy, TensorFlow, TFLearn, and some others for natural language processing (NLP) tasks.

### 2. Preparing Intents Data:

The code loads the intents from a JSON file and stores them in a variable called intents.

### 3. Preprocessing:

The code tokenizes each word in the sentences from the intents and stores them in lists words, classes, and documents.
It then performs stemming (finding the root of each word) and converts all words to lowercase while removing duplicates.

### 4. Creating Training Data:

The code creates training data in the form of a list of tuples (training), where each tuple contains the bag-of-words representation of the pattern and a one-hot encoded output representing the corresponding intent class.

### 5. Building and Training the Model:

The code defines a simple neural network architecture using TFLearn, with two hidden layers and a softmax output layer for multiclass classification.
The model is trained on the training data.

### 6. Saving Model and Pickle Data:

The trained model is saved to a file called 'model.tflearn'.
The words, classes, train_x, and train_y data are pickled (serialized) and saved to a file called 'training_data'.

### 7. Loading the Model and Pickle Data:

The model and the pickled data are loaded back into variables.

### 8. User Interaction Loop:

The code defines functions to clean up a user's input sentence and classify the intent based on the trained model's predictions.
The bot generates a response based on the detected intent.


