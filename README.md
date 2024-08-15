# YouTube Comment Scraper and Spam Detection

This repository contains two Jupyter notebooks and accompanying datasets designed to scrape YouTube comments and detect spam comments using machine learning.

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

### Spam Detection Model
The `spam-comments-detection-on-youtube.ipynb` notebook trains a machine learning model to detect spam in YouTube comments. It uses a dataset of labeled comments and applies feature extraction and model training using word embeddings and stylometric features. 

### YouTube Comment Scraper
The `youtube_comment_web_scraper.ipynb` notebook scrapes YouTube comments from specified videos or playlists. It uses the `youtube-comment-downloader` library to extract comments and saves them in a structured format (CSV). This data can be used to detect spam comments or perform other NLP tasks.

## Datasets

1. Training Data: 
   - Five Excel datasets downloaded from Kaggle [Images Dataset](https://www.kaggle.com/datasets/lakshmi25npathi/images). These datasets are pre-processed and used for training the spam detection model.
   
2. Scraped Data:
   - An Excel file containing YouTube comments, scraped using the YouTube Comment Scraper notebook.

## Installation and Setup

To set up this project, follow these steps:

1. Clone this repository:
    bash
    git clone https://github.com/yourusername/repository-name.git
    cd repository-name
 

2. Install the required dependencies:
    bash
    pip install -r requirements.txt


3. Install Jupyter notebook or VS Code with the Jupyter extension.

4. Set up Kaggle API credentials (if necessary) to download datasets.

## File Structure


├── datasets/
│   ├── kaggle_dataset_1.xlsx
│   ├── kaggle_dataset_2.xlsx
│   ├── kaggle_dataset_3.xlsx
│   ├── kaggle_dataset_4.xlsx
│   ├── kaggle_dataset_5.xlsx
│   ├── scraped_comments.xlsx
├── notebooks/
│   ├── youtube_comment_web_scraper.ipynb
│   ├── spam-comments-detection-on-youtube.ipynb
├── README.md
└── requirements.txt

## Usage

### 1. Scraping YouTube Comments

1. Open the `youtube_comment_web_scraper.ipynb` notebook.
2. Provide the video URLs or playlist URLs as input.
3. Run the notebook to scrape comments.
4. The comments will be saved in a CSV or Excel file for later use in training.

### 2. Training the Spam Detection Model

1. Ensure the datasets are correctly placed in the `datasets/` folder.
2. Open the `spam-comments-detection-on-youtube.ipynb` notebook.
3. Run the notebook to train the model. The training uses the datasets from Kaggle along with the scraped comments.
4. Evaluate the model performance and visualize results.

## Model Training

The spam detection model uses a combination of NLP techniques and machine learning algorithms. The model is trained on pre-labeled Kaggle datasets along with the scraped YouTube comments. The following steps are involved in training:

- Preprocessing comments (cleaning, tokenization)
- Feature extraction (word embeddings, stylometric features)
- Model training using algorithms like Logistic Regression, Random Forest, etc.
- Evaluation using metrics like accuracy.

## Results

- Accuracy: 89%

## Contributing

Contributions to this project are welcome. If you want to contribute, please follow these steps:

1. Fork the repository.
2. Create a new branch (`git checkout -b feature-branch`).
3. Commit your changes (`git commit -am 'Add some feature'`).
4. Push to the branch (`git push origin feature-branch`).
5. Create a pull request.

## License

This project is licensed under the MIT License - see the LICENSE file for details.
