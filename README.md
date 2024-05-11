
<H3>Name:D. Vishnu vardhan reddy</H3>
<H3>Register No:212221230023</H3>
<H3>Date:11/05/2024</H3>
<H1 Align="center">Project Based Experiment<H1>

## OBJECTIVE:
To perform sentiment analysis using your Facebook data and count the number of Occurrences of Your Name.
## PROGRAM:
```
import pandas as pd
from textblob import TextBlob

# Read data from CSV file
data = pd.read_csv("fb_sentiment.csv")

# Given name to count occurrences
given_name = "vishnu vardhan reddy"

# Initialize counters for sentiment analysis
sentiment_counts = {'positive': 0, 'negative': 0, 'neutral': 0}

# Initialize and Count occurrences for the given name
name_occurrences = sum(post.lower().count(given_name.lower()) for post in data['FBPost'])

# Perform sentiment analysis and count occurrences of the given name
for post in data['FBPost']:
    polarity = TextBlob(post).sentiment.polarity
    sentiment_counts['positive'] += polarity > 0
    sentiment_counts['negative'] += polarity < 0
    sentiment_counts['neutral'] += polarity == 0

# Print sentiment analysis results
print("Sentiment Analysis Results:")
for sentiment, count in sentiment_counts.items():
    print(f"{sentiment.capitalize()} sentiment: {count}")

# Print occurrences of the given name
print(f"Occurrences of '{given_name}': {name_occurrences}")

```

## OUTPUT:

<img width="370" alt="image" src="https://github.com/vishnudorigundla/Project-Based-Experiment-AAI/assets/94175324/effe9c51-53f8-4c8c-b580-a218f3d1fb05">



## INFERENCE:
By exploring sentiment analysis techniques and applying them to social media data, I gained practical experience in extracting sentiment information and identifying patterns in text. Additionally, counting occurrences of specific names enhanced my understanding of text processing and how to extract meaningful information from large datasets.
