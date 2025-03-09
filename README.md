# BigData-Team15-Project

## Description

This project produces a big data solution for bot identification in online marketplaces.
The dataset is sourced from https://www.kaggle.com/competitions/facebook-recruiting-iv-human-or-bot/data

## Files

- `Feature_Creation.ipynb`: This notebook performs initial feature engineering, producing `features.csv`
- `ML_Pipeline.ipynb`: This notebook ingests `features.csv` and produces a local and global approach random forest pipeline
- `bids.csv`, `train.csv`, `test.csv`: These CSV files contain the data used in the project, and can be downloaded from the Kaggle page above. Note that `bids.csv` in the submission contain first 500,000 rows, for testing purposes. To run on the full dataset download it from the link provided.

## How to Run

1. Download the data from Kaggle
2. Run the `Feature_Creation.ipynb` notebook to create features from the data.
3. Run the `ML_Pipeline.ipynb` notebook to partition and perform machine learning inference on the data.

NOTE: Files include large parameter grid searches, which you may wish to comment out before running, or only run selective cells.
It may also be desirable to comment out the time analysis functions, which are additionally time consuming.
`features.csv` is provided to use directly with ML_Pipeline, bypassing Feature_Creation.

## Dependencies

This project requires Python and the following Python libraries installed:

- numpy
- pandas
- pyspark
- scikit-learn
- matplotlib (optional, needed for plotting)
- seaborn (optional, needed for plotting)

You can install all these libraries at once using the provided `requirements.txt` file: 

```bash
pip install -r requirements.txt