# Purchase Intent Classifier

A machine learning project that predicts whether an online shopping visitor will make a purchase (Revenue = TRUE/FALSE) using a k-nearest neighbors classifier. Built with Python, pandas, and scikit-learn, it processes visitor session data and outputs purchase predictions with performance metrics.

## Problem

E-commerce platforms need to quickly understand which visitors are most likely to make a purchase. Accurately predicting purchase intent from real-time session behavior enables smarter decisions across the business, including:

- Targeted and efficient marketing
- Personalized on-site experiences
- Higher conversion through optimized user flows
- Better allocation of operational and advertising resources

This project builds a model that identifies high-intent shoppers based on their browsing patterns, helping e-commerce teams act proactively rather than reactively.

## Features

- Data preprocessing using pandas for efficient data handling
- K-Nearest Neighbors (KNN) classifier for purchase intent prediction
- Comprehensive evaluation metrics (sensitivity, specificity, accuracy)
- Clean, modular code structure

## Dataset

The dataset consists of 12,332 e-commerce visitor sessions, each represented as a single row. It includes 17 behavioral and contextual features:

- **Behavioral Features**: Administrative, Informational, and ProductRelated pages visited and their durations
- **Engagement Metrics**: BounceRates, ExitRates, PageValues
- **Contextual Features**: Month, OperatingSystems, Browser, Region, TrafficType
- **Visitor Characteristics**: VisitorType (Returning vs New), Weekend visit indicator
- **Target Variable**: Revenue (binary: TRUE/FALSE indicating purchase)

Dataset provided by Sakar, C.O., Polat, S.O., Katircioglu, M. et al., Neural Comput & Applic (2018).

## Installation

1. Clone this repository:

```bash
git clone <https://github.com/thekingslee/purchase-intent-classifier.git>
cd purchase-intent-classifier
```

2. Create a virtual environment (recommended):

```bash
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate
```

3. Install required dependencies:

```bash
pip install pandas scikit-learn
```

## Usage

1. Ensure the `shopping_data.csv` file is in the project directory
2. Open and run the `purchase-intent.ipynb` notebook
3. The notebook will:
   - Load and explore the data
   - Preprocess the features
   - Split data into training and test sets
   - Train the KNN classifier
   - Make predictions and evaluate performance

## Model

This project uses a **K-Nearest Neighbors (KNN) classifier** to predict purchase intent. The model is instance-based and non-parametric, relying on stored training examples rather than learning explicit parameters. With a default setting of `k = 3` (configurable), predictions are made by examining the nearest neighbors in feature space.

## Evaluation

The model is evaluated using metrics that highlight its ability to correctly identify both purchasing and non-purchasing visitors:

- **Sensitivity (True Positive Rate)**: Proportion of actual purchasers correctly identified
- **Specificity (True Negative Rate)**: Proportion of non-purchasers correctly identified
- **Correct/Incorrect Counts**: Overall accuracy breakdown

The evaluation includes division-by-zero handling for edge cases.

## Requirements

- Python 3.7+
- pandas
- scikit-learn

## File Structure

```
purchase-intent-classifier/
├── purchase-intent.ipynb    # Main notebook with analysis
├── shopping_data.csv         # Dataset
├── README.md                 # This file
└── .gitignore               # Git ignore file
```

## Acknowledgements

This project uses a dataset provided by Sakar, C.O., Polat, S.O., Katircioglu, M. et al., Neural Comput & Applic (2018).

## Contributing

Contributions, issues, and feature requests are welcome!
