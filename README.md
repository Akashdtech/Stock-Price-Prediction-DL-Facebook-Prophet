# Stock-Price-Prediction-DL-Facebook-Prophet
This project provides an end-to-end implementation of stock price analysis, prediction, and forecasting using machine learning and time-series modeling. It utilizes LSTM (Long Short-Term Memory) neural networks for predicting stock prices and Facebook's Prophet library for time-series forecasting.
Key Steps:

    Data Loading and Exploration:
        The dataset is loaded from a CSV file containing stock price data, including columns such as date, open, high, low, close, volume, and Name.
        Basic data exploration is performed to identify null values and understand the dataset's structure.

    Data Preprocessing:
        Date Conversion: The date column is converted to a datetime format for time-series analysis.
        Encoding Categorical Data: The Name column (categorical stock names) is one-hot encoded for model compatibility.
        Feature Scaling: Numerical columns (open, high, low, volume) are scaled using StandardScaler to normalize input features.

    LSTM Model for Stock Price Prediction:
        Data Preparation: The dataset is split into training and testing subsets. A portion of the data is selected to limit memory usage.
        LSTM Architecture:
            Three LSTM layers with 128, 256, and 128 units, followed by a dropout layer to reduce overfitting.
            A fully connected layer outputs a single continuous value (stock price).
        Model Compilation and Training: The model uses the Adam optimizer and Mean Squared Error (MSE) as the loss function.
        Evaluation Metrics: After training, the model is evaluated on the test set using:
            Mean Squared Error (MSE)
            Root Mean Squared Error (RMSE)
            Mean Absolute Error (MAE)

    Prophet Model for Time-Series Forecasting:
        Dataset Preparation: A subset of data with columns date and close is reformatted for Prophet, with column names renamed to ds (date) and y (target variable).
        Forecasting:
            Prophet is used to fit the historical data and forecast stock prices for the next 365 days.
            The forecast includes components like trend, seasonal variations, and other time-series elements.
        Visualization:
            Forecast results and individual time-series components are visualized using Prophet's plotting tools.

This project demonstrates how to combine deep learning and time-series forecasting techniques to predict and analyze stock prices effectively.
