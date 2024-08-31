# Sentimental_analysis
# Sentiment Analysis on Kaggle Dataset

## Overview

This project implements a sentiment analysis tool that processes text data from a Kaggle dataset using Python. It leverages the VADER (Valence Aware Dictionary and sEntiment Reasoner) sentiment analysis library from the NLTK (Natural Language Toolkit) library to classify text as positive, negative, or neutral based on the sentiment expressed.

## Features

- **Sentiment Classification**: Analyzes the sentiment of text data, categorizing each entry into positive, negative, or neutral.
- **Score Generation**: Produces a compound score for each text, indicating the strength and direction of the sentiment.
- **CSV Output**: Saves the results, including the original text, its corresponding sentiment, and the sentiment score, to a new CSV file for further analysis.

## Requirements

To run this project, ensure you have the following:

- Python 3.6 or higher
- Pandas library
- NLTK library
- VADER sentiment analysis tool from NLTK

## Installation

1. **Clone the repository** (if applicable):
   ```bash
   git clone <[repository-url](https://github.com/Praful-John2409/Sentimental_analysis)>
   cd <repository-directory>
   ```

2. **Install the required libraries**:
   ```bash
   pip install pandas nltk
   ```

3. **Download the VADER lexicon**:
   In your Python environment, run:
   ```python
   import nltk
   nltk.download('vader_lexicon')
   ```

## Dataset

- The dataset used in this project should be a CSV file containing a column named `text`, which includes the text entries to be analyzed.
- You can specify the path to your dataset CSV file in the code.

## Usage

1. **Modify the file path**: Ensure that the file path in the code points to your dataset CSV file.
   ```python
   dataset = pd.read_csv(r'your_dataset_location')
   ```

2. **Run the script**:
   Execute the Python script. The program will read the dataset, perform sentiment analysis on each text entry, and save the results to a new CSV file.

   ```python
   if __name__ == "__main__":
       print("Testing sentiment analysis on Kaggle dataset:")
       test_on_kaggle_dataset()
   ```

3. **Check the output**: The results will be saved in a new CSV file in the same directory as the input file, with columns for the original text, sentiment classification, and sentiment score.

## Example Output

The output CSV file will have the following structure:

| text                   | sentiment | score  |
|------------------------|-----------|--------|
| "I love this product!" | positive  | 0.765  |
| "This is the worst!"   | negative  | -0.750 |
| "It's okay."           | neutral   | 0.000  |

## Error Handling

The script includes error handling for common issues such as:
- **FileNotFoundError**: Triggered if the specified CSV file does not exist.
- **PermissionError**: Triggered if the script lacks the necessary permissions to access the file.
- **General Exception Handling**: Catches any other unexpected errors and displays a relevant message.

## Conclusion

This sentiment analysis tool provides a straightforward way to evaluate and categorize sentiments in text data, making it useful for various applications such as market research, customer feedback analysis, and social media sentiment tracking.

## License

This project is licensed under the MIT License - see the LICENSE file for details.

---
