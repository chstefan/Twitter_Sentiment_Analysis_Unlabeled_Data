# Twitter Sentiment Analysis with BERT

This project focuses on performing sentiment analysis on Twitter data using a BERT model, which is a deep learning approach developed by Google for natural language processing (NLP). The objective is to classify tweets into various sentiment categories: Positive, Neutral, Negative, and Irrelevant. This guide will walk you through the process of setting up the project, training the BERT model, and evaluating its performance.

## Project Structure

- **Data**: The dataset consists of Twitter messages with corresponding sentiment labels. Data files should be placed in the `Data Analytics Portfolio für Git/Unsupervised Learning` directory.
- **Scripts**: The main Python script for training and evaluating the model is provided.
- **Results**: Model checkpoints and logs are saved to the `./results` and `./logs` directories, respectively.

## Requirements

- Python 3.8 or higher
- pandas
- scikit-learn
- transformers
- datasets

You can install the required packages using pip:

```bash
pip install pandas scikit-learn transformers datasets

##Data Preparation

The dataset should be in CSV format with columns for ID, Topic, Sentiment, and Text. The script expects two files:

twitter_training.csv: Used for training the model.
twitter_validation.csv: Used for validating the model's performance.
Make sure to update the paths to these files in the script if necessary.

##Model Training

The script uses the BertForSequenceClassification model from the Hugging Face transformers library, pre-trained on the bert-base-uncased model. The training process includes tokenizing the tweets, encoding the sentiments, and fine-tuning the BERT model for classification.

To start training the model, run the Python script:
python sentiment_analysis.py

##Evaluation

After training, the model's performance is evaluated on the validation dataset using accuracy and a classification report, which includes precision, recall, and F1-score for each sentiment category.

##Customization

You can adjust the training parameters in the TrainingArguments class instance to experiment with different configurations, such as the number of epochs, batch size, and learning rate.

##License

This project is open-source and available under the MIT License. Feel free to use, modify, and distribute the code as you see fit.

##Contribution

Contributions to the project are welcome! Whether it's reporting a bug, discussing improvements, or submitting a pull request, all contributions are appreciated.
