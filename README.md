# Stock Market Directional Predictor

This is a semester project for the CS 5805 Machine Learning course at Virginia Tech.

The goal of this project is to develop and evaluate machine learning models to predict the direction (up or down) of daily stock prices. This project uses a Long Short-Term Memory (LSTM) network using PyTorch and compares various evaluation metrics with baseline models such as Logistic Regression, SVM, and Random Forest from Scikit-learn.

### Project Structure (after running both notebooks)

```
cs5805stockpredictor/
├── notebooks/
│   ├── 1_data_cleaning.ipynb
│   └── 2_baseline_and_lstm_models.ipynb
├── data/
│   └── raw/                # Stock data from Kaggle
│   └── processed/          # Cleaned CSVs
├── models/
├── outputs/
│   └── figures/            # Performance visuals
│   └── metrics/            # Compares models
├── requirements.txt
└── README.md
```

### How to run this project

1. Clone this repository and create data folder:

```
git clone https://github.com/migmagtoto/cs5805stockpredictor
cd cs5805stockpredictor
mkdir data
```

2. Download and upload stock data from Kaggle:

- Open https://www.kaggle.com/datasets/borismarjanovic/price-volume-data-for-all-us-stocks-etfs in a browser
- Log in and click `Download` and `Download dataset as zip`
- In File Explorer, unzip the downloaded `archive.zip`, open the `archive` folder, and move/drag the `Stocks` folder into `data`
- Rename `Stocks` to `raw`

3. Create a virtual environment:

```
# for Linux/macOS:
python3 -m venv venv
source venv/bin/activate

# for Windows:
python -m venv venv
venv\Scripts\activate
```

4. Install dependencies:

```
pip install --upgrade pip
pip install -r requirements.txt
```

5. Run Jupyter Notebooks:

- Start Jupyter: `jupyter lab`
- Run `notebooks/1_data_cleaning.ipynb`: Preprocesses raw stock data and generates `train.csv`, `val.csv`, and `test.csv`
- Run `notebooks/2_baseline_and_lstm_models.ipynb`: Takes those .csv files and trains baseline and LSTM models