#Audiobook Customer Classification

Overview
This project aims to predict whether customers will buy audiobooks again based on various features such as their purchasing behavior, amount spent, and engagement metrics. The classification model is trained using a dataset obtained from audiobook customer transactions.

Dataset Content
The dataset Audiobooks_data.csv contains information about customers' interactions with an audiobook service. Each row represents a customer transaction and includes the following features:

Customer ID: Unique identifier for each customer.
Book Length (mins): Total duration of audiobooks purchased by the customer.
Book Price ($): Price paid for the audiobooks.
Avg. Minutes Listened: Average duration of audiobooks listened to by the customer.
Completion: Percentage of audiobooks completed by the customer.
Support Requests: Number of customer support requests made by the customer.
Last Visit Mins: Minutes since the customer's last visit to the service.
Purchase Class: Target variable indicating whether the customer made another purchase (0: No, 1: Yes).

Data Preprocessing
The preprocessing steps involve loading the raw CSV data, removing instances with unbalanced target classes to achieve equal priors, and normalizing the input features.

Model Architecture
The classification model consists of an input layer with 7 nodes (corresponding to the features), two hidden layers with 40 nodes each using ReLU activation, and an output layer with 2 nodes and softmax activation for classification.

Training and Evaluation
The model is trained using the Adam optimizer and sparse categorical cross-entropy loss function. Training parameters include a batch size of 1000, early stopping to prevent overfitting, and a maximum of 100 epochs. Model performance is evaluated on the validation set to monitor accuracy and loss, and further assessed on the test set for generalization ability.
