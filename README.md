# Email Spam Classifier

![Email Spam Classifier](https://t3.ftcdn.net/jpg/09/20/22/64/360_F_920226428_V01z4i1KrONjr0pBwVaWw9OHt4hjM2ga.jpg)

## Project Overview
The Email Spam Classifier project is designed to build a machine learning model capable of accurately classifying emails as spam or non-spam (ham). The increasing volume of unsolicited emails highlights the need for automating email classification to improve user experience and productivity.

## Steps Involved in the Project

### 1. Data Loading
The project begins by loading a CSV file containing email data using pandas. The dataset's structure is explored to understand its contents, setting the foundation for further analysis.

### 2. Data Preprocessing
Preprocessing involves cleaning the dataset by removing unnecessary columns and renaming the relevant ones. Missing and duplicate values are addressed to ensure the dataset is reliable, improving model performance.

### 3. Exploratory Data Analysis (EDA)
EDA is performed to understand the data distribution. Visualizations like pie charts are used to examine the balance between spam and ham emails. This step identifies potential biases in the dataset and helps inform the modeling approach.

### 4. Text Transformation
Text data is preprocessed to prepare it for machine learning:
- **Lowercasing**: Ensures consistency by converting all text to lowercase.
- **Tokenization**: Splits text into individual words using the Bag of Words model.
- **Alphanumeric Filtering**: Removes non-alphanumeric characters to focus on meaningful words.
- **Stop Words Removal**: Eliminates common, non-informative words such as "and," "the," etc.

These transformations clean and standardize the data, enhancing model training.

### 5. Feature Extraction
After text transformation, the text is converted into numerical features using methods like **TF-IDF** (Term Frequency-Inverse Document Frequency), which reflects word importance and improves model understanding of the text.

### 6. Naive Bayes Algorithms
Three types of Naive Bayes algorithms are used:
1. **Gaussian Naive Bayes**: Assumes normally distributed features and is effective for continuous data.
2. **Multinomial Naive Bayes**: Best suited for discrete features, such as word counts, making it ideal for text classification.
3. **Bernoulli Naive Bayes**: Works well with binary features, focusing on whether a word appears in an email.

### 7. Model Training and Evaluation
The models are trained on the dataset, with performance evaluated using metrics like:
- **Accuracy**: Measures the overall correctness of the model.
- **Precision**: The proportion of correct spam classifications.
- **F1 Score**: The harmonic mean of precision and recall, useful for imbalanced datasets.

## Results
- **Accuracy**: 98% on the test dataset.
- **Precision**: 94% on the test dataset.

Comparison of the algorithms:
- **Multinomial Naive Bayes**: Best performance in precision and F1 score, making it the most effective for spam classification.
- **Gaussian Naive Bayes**: Performed reasonably well but did not match the Multinomial version due to assumptions about feature distributions.
- **Bernoulli Naive Bayes**: Competitive in identifying word presence but underperformed in overall accuracy.

## Conclusion
The project successfully built an effective email spam classifier by following essential steps: data loading, preprocessing, text transformation, feature extraction, model training, and evaluation. The Multinomial Naive Bayes algorithm demonstrated the best performance, highlighting its suitability for text classification tasks.

This project offers valuable insights into text classification challenges and demonstrates the significance of selecting the right algorithms based on data characteristics.
