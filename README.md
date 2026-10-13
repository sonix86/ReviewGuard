# ReviewGuard
AI-powered product review analysis using language models and machine learning

# About the Project

The app will help small online shop owners understand what customers think about their products. It will analyse reviews in Uzbek and Russian, predict positive or negative sentiment and show how repeated texts affect the results.

ReviewGuard will not decide whether a review is fake. It will only find exact repeated texts and compare the results before and after excluding repeated copies (within rising the flag under the suspicious comments).

# How It Works

This project uses two AI areas.

**1. Language Models**

I plan to use a pretrained model called `multilingual-e5-small`. It turns review text into numerical embeddings.

**2. Classical Machine Learning**

I will train a Logistic Regression classifier using these embeddings. The classifier will predict whether a review is positive or negative.

The process is:

`Review text → Language Model → Embeddings → Logistic Regression → Sentiment prediction`

A separate rule will be used to find exact repeated texts.

## Dataset

I will use the [Uzbek Sentiment Analysis dataset](https://github.com/sssplash6/uzbek-sentiment-analysis).

The file I checked is `uzum_reviews_binary.csv`. It contains 1,172 product reviews:

- 930 positive reviews
- 242 negative reviews

The dataset contains both Uzbek and Russian reviews. I will clean the data before training and testing the model.

## Planned Features

- Upload a CSV file with product reviews.
- Predict positive or negative sentiment.
- Find exact repeated texts.
- Compare results before and after excluding repeated copies.
- Show positive and negative review counts and percentages.
- Calculate the average rating when ratings are available.
- Display each review, its predicted sentiment and its repeated-text flag.

The first version will support up to 500 reviews per upload.

## Technologies

- Python and other features

## Model Evaluation

I will split the data into training, validation and test sets. I will compare Logistic Regression with a simple baseline that predicts the most common class.

I will use accuracy, macro F1 and a confusion matrix to evaluate the model. I will add the actual results after testing.

## Limitations

- The model may make incorrect predictions.
- Some Uzbek reviews may be difficult to classify.
- The first version will detect exact repeated texts, not similar texts with different wording.
- Repeated text does not necessarily mean a review is fake.
- The model will predict only positive or negative sentiment.

## Data and Privacy

I will cite the dataset source and follow its licence requirements. I will avoid publishing the full dataset in this repository.

Uploaded reviews will not be intentionally saved or logged by the app.

## Project Status

This project is being developed as part of my AI course. My goal is to build a working app, test the model and deploy it so that other people can use it.

## AI Tools

I used ChatGPT to help refine the project idea and prepare the documentation. 
