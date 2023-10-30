# Implementation-of-Sentimental-Analysis
// Type the description of Sentimental Analysis process
## Program:
```
import pandas as pd
import vaderSentiment as vs

# Read the Excel file
df = pd.read_excel('output.xlsx')

# Create a VADERSentiment object
analyzer = vs.vaderSentiment.SentimentIntensityAnalyzer()

# Calculate the sentiment scores for each text
sentiment_scores = []
for text in df['Text']:
    sentiment_scores.append(analyzer.polarity_scores(text))

# Create a list of the texts
texts = list(df['Text'])

# Display the sentiment scores for each text
for text, sentiment_score in zip(texts, sentiment_scores):
    print("\n\nText:", text)
    print("Positive:", sentiment_score['pos'])
    print("Negative:", sentiment_score['neg'])
    print("Neutral:", sentiment_score['neu'])
    print("Compound:", sentiment_score['compound'])
```
## Output:

![image](https://github.com/VarshaAjith1110/Implementation-of-Sentimental-Analysis/assets/94222288/f3d9c066-dd73-4c4f-b6ea-afffbd105633)

