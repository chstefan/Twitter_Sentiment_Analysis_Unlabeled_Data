# Twitter_Sentiment_Analysis_Unlabeled_Data

# Data Loading:
Imported the pandas library for data manipulation and analysis.
Loaded the Twitter training and validation datasets from CSV files using pd.read_csv().
#Data Inspection and Preliminary Analysis:
Printed the first few rows of both datasets with .head() to get an initial look at the data structure.
Checked for missing values in both datasets using .isnull().sum() to identify data completeness.
# Data Cleaning and Preparation:
Assigned new column names (ID, Topic, Sentiment, Text) to both datasets for clarity.
Removed rows from the training dataset where the Text column was missing, as these entries are not useful for sentiment analysis.
# Sentiment Analysis Setup:
Imported the pipeline function from the Hugging Face transformers library to utilize pre-trained models for sentiment analysis.
Initialized the sentiment analysis pipeline, specifying the use of PyTorch (framework="pt") to ensure compatibility with the deep learning library being used.
# Sentiment Prediction:
Defined a function predict_sentiment to apply the sentiment analysis pipeline to a piece of text, returning the model's sentiment label (e.g., POSITIVE, NEGATIVE).
Applied this function to the Text column of the validation dataset, storing the predictions in a new column, Predicted_Sentiment.
# Validation and Accuracy Assessment:
Mapped manually labeled sentiments in the validation dataset to match the format of the model's predicted sentiments (if necessary).
Calculated the accuracy of the model's predictions compared to the manual labels to assess how well the model performed.
Generated a detailed classification report providing precision, recall, and F1-score for each sentiment class, offering a deeper insight into the model's performance.
