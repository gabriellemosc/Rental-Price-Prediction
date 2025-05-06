# Property Price Prediction (Airbnb)

### Context

On Airbnb, anyone who owns a room or a property (apartment, house, cottage, inn, etc.) can list it to be rented by the day.

You create your host profile (the person who makes a property available for daily rental) and create your property listing.

In this listing, the host should describe the property's features as completely as possible, helping guests choose the most suitable place (and making the listing more attractive).

There are dozens of customization options, such as minimum stay, price, number of rooms, cancellation rules, extra guest fees, ID verification requirements, and more.

### Our Goal

To build a price prediction model that helps an ordinary person estimate how much they should charge per night for their property.

Or, for guests, to identify whether a given property is well-priced (below the average for similar listings) or overpriced.

### Available Resources, Inspiration and Credits

The datasets used in this project were obtained from Kaggle: https://www.kaggle.com/allanbruno/airbnb-rio-de-janeiro

## Table of Contents

- [Context](#context)
- [Project Structure](#project-structure)
- [Libraries Used](#libraries-used)
- [How to Run the Project](#how-to-run-the-project)
- [Model Details](#model-details)
- [Contribution](#contribution)
- [License](#license)

## Project Structure

- `deployprojeto.py`: Main script implementing the prediction interface using Streamlit.
- `modelo.joblib`: File containing the trained model (ExtraTreesRegressor).
- `dados.csv`: Dataset used for training and testing the model.
- `README.md`: Project documentation file.

## Libraries Used

The following Python libraries were used to build this project:

- `pandas`: Data manipulation and analysis.
- `pathlib`: Handling of file and directory paths.
- `numpy`: Numerical computing.
- `seaborn`: Data visualization built on matplotlib.
- `matplotlib`: Library for static, animated, and interactive plots.
- `plotly`: Interactive graphing library.
- `scikit-learn`: Machine learning tools for data analysis and predictive modeling.
- `gc`: Interface for Python's garbage collection.
- `streamlit`: Framework for building interactive web apps for data science.

## How to Run the Project

### Prerequisites

- Python 3.x
- Install the required libraries:

```bash
pip install pandas numpy seaborn matplotlib plotly scikit-learn streamlit joblib
```

## The Interface for Making New Predictions
![GUI of the forecast price](https://github.com/gabriellemosc/Rental-Price-Prediction/blob/main/Captura%20de%20tela%202024-08-25%20151801.png)

## Model Details

The model used for price prediction is the **ExtraTreesRegressor**, trained on the available `dados.csv` dataset. Property features such as latitude, longitude, number of bedrooms, property type, among others, are used as input variables.

### Evaluation Metrics

The model’s performance was assessed using the following metrics:

- **R² (R-Squared)**: Measures how well the model fits the observed data. A higher R² means better explanatory power.
- **RMSE (Root Mean Squared Error)**: Indicates the average magnitude of the error between predicted and actual prices. Lower RMSE means better model accuracy.
