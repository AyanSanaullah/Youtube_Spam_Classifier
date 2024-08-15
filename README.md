# YouTube Spam, Hate, and Sentiment Classifier

This repository contains two Jupyter notebooks and accompanying datasets designed to scrape YouTube comments and detect spam, classify hate speech, and analyze sentiment in comments using machine learning.

## Table of Contents

1. [Project Overview](#project-overview)
2. [Datasets](#datasets)
3. [Installation and Setup](#installation-and-setup)
4. [File Structure](#file-structure)
5. [Usage](#usage)
6. [Model Training](#model-training)
7. [Results](#results)
8. [Contributing](#contributing)
9. [License](#license)

## Project Overview

### Spam, Hate Speech, and Sentiment Detection Model
The `spam-comments-detection-on-youtube.ipynb` notebook trains a machine learning model to classify YouTube comments into multiple categories:
- **Spam Detection:** Identifies spam comments.
- **Hate Speech Detection:** Flags comments containing hate speech.
- **Sentiment Analysis:** Classifies comments as positive, negative, or neutral.

It uses a dataset of labeled comments and applies feature extraction and model training using word embeddings, stylometric features, and various machine learning algorithms.

### YouTube Comment Scraper
The `youtube_comment_web_scraper.ipynb` notebook scrapes YouTube comments from specified videos or playlists. It uses the `youtube-comment-downloader` library to extract comments and saves them in a structured format (CSV). While optional, this tool allows users to scrape their own datasets for further spam, hate speech, and sentiment analysis.

## Datasets

1. **Training Data:** 
   - Five Excel datasets downloaded from Kaggle's [Images Dataset](https://www.kaggle.com/datasets/lakshmi25npathi/images). These datasets are pre-processed and used for training the spam, hate speech, and sentiment detection models.
   
2. **Scraped Data (Optional):**
   - You may scrape your own YouTube comments using the YouTube Comment Scraper notebook. The scraped data can be used as additional input for classification tasks.

## Installation and Setup

To set up this project, follow these steps:

1. Clone this repository:
    ```bash
    git clone https://github.com/AyanSan/Youtube_Spam_Classifier
    cd Youtube_Spam_Classifier
    ```

2. Install the required dependencies:
    ```bash
    pip install -r requirements.txt
    ```

3. Install Jupyter notebook or VS Code with the Jupyter extension.

4. (Optional) Set up Kaggle API credentials to download datasets.

## File Structure

```plaintext
├── datasets/
│   ├── kaggle_dataset_1.xlsx
│   ├── kaggle_dataset_2.xlsx
│   ├── kaggle_dataset_3.xlsx
│   ├── kaggle_dataset_4.xlsx
│   ├── kaggle_dataset_5.xlsx
│   ├── scraped_comments.xlsx (optional)
├── notebooks/
│   ├── youtube_comment_web_scraper.ipynb
│   ├── spam-comments-detection-on-youtube.ipynb
├── README.md
└── requirements.txt
```

## Usage

### 1. Scraping YouTube Comments (Optional)

1. Open the `youtube_comment_web_scraper.ipynb` notebook.
2. Provide the video URLs or playlist URLs as input.
3. Run the notebook to scrape comments.
4. The comments will be saved in a CSV or Excel file.

### 2. Training the Spam, Hate Speech, and Sentiment Detection Model

1. Ensure the datasets are correctly placed in the `datasets/` folder.
2. Open the `spam-comments-detection-on-youtube.ipynb` notebook.
3. Run the notebook to train the model. The training uses the Kaggle datasets and any additional scraped data.
4. Evaluate the model performance and visualize results.

## Model Training

The detection model uses a combination of natural language processing (NLP) techniques and machine learning algorithms. The following steps are involved in training:

- Preprocessing comments (cleaning, tokenization)
- Feature extraction (word embeddings, stylometric features)
- Model training using algorithms like Logistic Regression, Random Forest, etc.
- Multi-task learning for spam detection, hate speech detection, and sentiment classification.
- Evaluation using metrics like accuracy, precision, recall, and F1-score.

## Results

- **Spam Detection Accuracy:** 89%
- **Hate Speech Detection Accuracy:** Pretrained
- **Sentiment Analysis Accuracy:** Pretrained

## Contributing

Contributions to this project are welcome. If you want to contribute, please follow these steps:

1. Fork the repository.
2. Create a new branch (`git checkout -b feature-branch`).
3. Commit your changes (`git commit -am 'Add some feature'`).
4. Push to the branch (`git push origin feature-branch`).
5. Create a pull request.

## License

This project is licensed under the MIT License - see the LICENSE file for details.
