📊 About the Dataset:

I  got this dataset from this link: [https://www.kaggle.com/datasets/ronikdedhia/fake-news?utm_source=chatgpt.com
](url)

id: Unique id for a news article

title: Title of the news article

author: Author of the news article

text: Main text/content of the article (could be incomplete)

label: Binary label indicating if the article is fake or real

1 → Fake News

0 → Real News

🧹 Data Preprocessing

Removed missing values and duplicates

Applied Stemming: Reduced words to their root form (e.g., Actor, Actress, Acting → Act)

Cleaned text (lowercase, removed special characters and stopwords)

📂 Model Building

Split dataset into training and test sets

Trained a Logistic Regression model using scikit-learn

📈 Model Evaluation

Calculated accuracy score on test data

Built a predictive system to classify new input text as fake or real
