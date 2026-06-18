# Data Access

## Source

Dataset name: ChatGPT reviews [DAILY UPDATED]

Source URL: https://www.kaggle.com/datasets/ashishkumarak/chatgpt-reviews-daily-updated

Author / Organization: kaggle

License:

## Files

Expected files after download:

* chatgpt_reviews.csv

## Local Organization

Raw files should be placed in:

01_data/raw/

Processed files should be placed in:

01_data/processed/

## Access

### Manual Download

Navigate to the Kaggle dataset page:

https://www.kaggle.com/datasets/ashishkumarak/chatgpt-reviews-daily-updated

Click Download.
Extract the downloaded archive.

Place the file:

chatgpt_reviews.csv

into:

01_data/raw/


### Automated Download (Optional)
Automated Download (Optional)

If the Kaggle API is configured, the dataset can be downloaded directly from the command line.

Example:

kaggle datasets download ashishkumarak/chatgpt-reviews-daily-updated

After download:

Extract the archive.

Move chatgpt_reviews.csv into:

01_data/raw/

Requirements:

Kaggle account
Kaggle API credentials (kaggle.json)
Kaggle CLI installed and configured

## Notes

* Raw data excluded from Git via `.gitignore`.
* Environment reproducibility documented in `environment.yml`.
* This file documents how to obtain the original dataset.
