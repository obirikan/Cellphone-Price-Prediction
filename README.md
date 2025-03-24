# Cellphone Price Prediction

This project uses **Linear Regression** to predict cellphone prices based on various features such as resolution, RAM, battery capacity, and more. The best model is selected through multiple training iterations and saved for future use.

## Features
- Uses **Linear Regression** to predict phone prices.
- Trains the model multiple times and selects the best one.
- Saves and loads the trained model using **pickle**.
- Uses **scikit-learn** for machine learning.

## Requirements
Ensure you have the following dependencies installed:
```bash
pip install pandas numpy scikit-learn matplotlib
```

## Dataset
The dataset should be in a CSV file named **Cellphone.csv**, containing the following columns:
- `Product_id`
- `Price` (Target Variable)
- `Sale`
- `thickness`
- `weight`
- `resoloution`
- `ppi`
- `cpu core`
- `cpu freq`
- `internal mem`
- `ram`
- `RearCam`
- `Front_Cam`
- `battery`

## Usage
### 1. Train the Model
Run the script to train the model and save the best one:
```bash
python train.py
```
The script:
- Loads the dataset
- Splits it into training and testing sets
- Trains the model multiple times
- Saves the best-performing model

### 2. Predict with the Saved Model
To use the saved model for prediction:
```python
saved_model = open('studentmodel.pickle', 'rb')
new_model = pickle.load(saved_model)

sample_input = [[5, 401, 4, 2, 16, 2, 16, 8, 2500]]
predicted_price = new_model.predict(sample_input)
print("Predicted Price:", predicted_price)
```

## Code Overview
### **Training Process**
- Load dataset from `Cellphone.csv`
- Drop unnecessary columns
- Split data into training and test sets
- Train the model multiple times and save the best one

### **Model Prediction**
- Load the trained model
- Predict prices based on input features

## Example Output
```
Predicted: 450.25 | Features: [5, 401, 4, 2, 16, 2, 16, 8, 2500] | Actual: 460
Predicted: 520.10 | Features: [6, 350, 6, 3, 32, 4, 20, 12, 3000] | Actual: 530
```

## License
This project is open-source and available under the **MIT License**.

## Author
Developed by **[Your Name]**.

