# Housing Data Prediction Model

This repository contains a predictive model for housing prices based on several features of the properties, such as number of rooms, square footage, location, etc. The model was built using Python and several machine learning libraries, and it was trained on a dataset of housing prices and features from several cities in the US.

## Usage

To use the model, you can either clone this repository or download the `model.py` file. Then, you can import the `HousingPredictor` class from the file and create an instance of it, passing the path to the dataset file as a parameter:

```python
from model import HousingPredictor

predictor = HousingPredictor('path/to/dataset.csv')
```

After creating the predictor object, you can call its `predict` method to get a predicted price for a given set of features:

```python
features = {'rooms': 3, 'square_feet': 1500, 'city': 'Boston', 'zipcode': '02115'}
predicted_price = predictor.predict(features)
print(f"Predicted price: {predicted_price}")
```

## Dataset

The dataset used to train the model is included in the repository as `dataset.csv`. It contains over 10,000 rows of housing prices and features from several US cities, such as Boston, New York, San Francisco, etc. The columns of the dataset are:

- `rooms`: number of rooms in the property.
- `square_feet`: total square footage of the property.
- `city`: city where the property is located.
- `zipcode`: ZIP code of the property.
- `price`: sale price of the property.

## Model

The model used in this project is a Random Forest Regressor, implemented using the Scikit-Learn library. The model achieved an R-squared score of 0.82 on the training data and 0.78 on the test data, indicating a good fit and generalization performance.

The `model.py` file also contains some utility functions for data preprocessing and feature engineering, as well as for loading and saving the model using the Pickle library.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
