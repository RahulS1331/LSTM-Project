# Next Word Prediction Using LSTM

## Project Overview
This project aims to develop a deep learning model for predicting the next word in a given sequence of words. The model is built using Long Short-Term Memory (LSTM) networks, which are well-suited for sequence prediction tasks.

### Steps Involved:

1. **Data Collection**: 
   - We use the text of Shakespeare's "Hamlet" as our dataset. This rich, complex text provides a good challenge for our model.

2. **Data Preprocessing**:
   - The raw text data undergoes several preprocessing steps to prepare it for model training:
     - **Tokenization**: Breaking down the text into individual words (tokens).
     - **Sequence Creation**: Converting the tokens into sequences of a fixed length.
     - **Padding**: Ensuring all input sequences have uniform length by padding shorter sequences.
     - **Splitting**: Dividing the data into training and testing sets to facilitate model evaluation.

3. **Model Building**:
   - An LSTM-based neural network model is constructed with the following architecture:
     - **Embedding Layer**: Converts input words into dense vectors of fixed size.
     - **LSTM Layers**: Two stacked LSTM layers capture temporal dependencies in the data.
     - **Dense Output Layer**: A fully connected layer with a softmax activation function outputs the probability distribution over the next possible words.

4. **Model Training**:
   - The model is trained on the preprocessed data with the following considerations:
     - **Loss Function**: Categorical cross-entropy is used to measure the difference between predicted and actual word distributions.
     - **Optimizer**: Adam optimizer is employed for efficient gradient descent.
     - **Early Stopping**: Implemented to prevent overfitting by monitoring the validation loss and halting training when improvement stalls.

5. **Model Evaluation**:
   - Post-training, the model's performance is assessed using a set of example sentences. The evaluation focuses on the model's ability to accurately predict the next word in various contexts.

6. **Deployment**:
   - A Streamlit web application is developed to provide an interactive interface for users. The application allows users to input a sequence of words and receive real-time predictions for the next word.

## How to Run the Project

### Prerequisites
- Python 3.6 or higher
- pip (Python package installer)

### Installation Steps

1. **Clone the Repository**:
   ```bash
   git clone https://github.com/RahulS1331/LSTM-Project.git
   cd LSTM-Project
