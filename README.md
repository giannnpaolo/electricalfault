# Predicting Electrical Faults Using Machine Learning

## Overview

This project aims to develop a machine learning model to accurately predict transmission line faults. The model leverages various real world features including engineered features to identify and predict potential faults in transmission lines, which can help in preemptive maintenance and reducing downtime.

## Table of Contents

- [Overview](#overview)
- [Project Structure](#project-structure)
- [Installation](#installation)
- [Data](#data)
- [Methodology](#methodology)
- [Results](#results)
- [Explainability](#explainability)
- [Usage](#usage)
- [Contributing](#contributing)
- [License](#license)
- [Acknowledgments](#acknowledgments)

## Project Structure

```
electrical-faults/
├── README.md                    # Project overview and instructions
├── requirements.txt             # Required Python packages
├── ML1 Project Notebook- Servanez, GPT.ipynb  # Project Notebook
├── ML1 Project Presentation - Servanez, GPT.pdf # Project Report Presentation
```

## Installation

To get started with this project, follow these steps:

1. **Clone the repository**:
    ```
    git clone https://github.com/yourusername/predicting-electrical-faults.git
    cd predicting-electrical-faults
    ```

2. **Create and activate a virtual environment**:
    ```
    python -m venv venv
    source venv/bin/activate  # On Windows, use `venv\Scripts\activate`
    ```

3. **Install the required packages**:
    ```
    pip install -r requirements.txt
    ```

## Data

The data used in this project consists of geospatial features and historical transmission line fault records. The dataset is stored in the `data/raw` directory and should be preprocessed before model training.

## Methodology

1. **Data Preprocessing**: 
    - Load and clean the data.
    - Handle missing values and outliers.
    - Feature engineering to create relevant features.

2. **Exploratory Data Analysis (EDA)**:
    - Analyze data distribution and relationships between features.
    - Visualize important patterns and insights.

3. **Model Training**:
    - Split the data into training and testing sets.
    - Train an XGBoost model on the training data.
    - Evaluate the model's performance using appropriate metrics.

4. **Explainability**:
    - Apply explainability techniques to understand the model's predictions.
    - Identify key predictors influencing electrical faults.

## Results

The XGBoost model achieved a high accuracy in predicting electrical faults, outperforming traditional methods. Key predictors identified include:
- Geospatial features
- Historical fault records
- Environmental conditions

## Explainability

Explainability techniques, such as SHAP (SHapley Additive exPlanations), were used to interpret the model's predictions. The main drivers of predictions include:
- Distance to substations
- Line age
- Environmental factors (e.g., weather conditions)

## Usage

To use the model for predicting electrical faults, follow these steps:

1. **Preprocess the data**:
    ```python
    from src.data_preprocessing import preprocess_data
    data = preprocess_data('data/raw/dataset.csv')
    ```

2. **Train the model**:
    ```python
    from src.model import train_model
    model = train_model(data)
    ```

3. **Make predictions**:
    ```python
    predictions = model.predict(new_data)
    ```

## Contributing

Contributions are welcome! Please read the [contributing guidelines](CONTRIBUTING.md) before getting started.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for more details.

## Acknowledgments

Special thanks to all contributors and data providers for making this project possible.

---
