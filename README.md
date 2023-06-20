# Diabetesprediction
Data Loading: The project reads a diabetes dataset stored in a CSV file using the `read_csv` function from the `pandas` library. The dataset is loaded into a DataFrame, which is a two-dimensional data structure. The features (X) and the outcome (Y) are extracted from the DataFrame.

Data Preparation: To ensure that all features are on a similar scale, the features are standardized using the `StandardScaler` class from the `sklearn.preprocessing` module. Standardization involves subtracting the mean and dividing by the standard deviation for each feature.

Train-Test Split: The dataset is split into training and testing sets using the `train_test_split` function from the `sklearn.model_selection` module. This function randomly divides the data into two sets based on a specified test size (in this case, 20%) while maintaining the proportion of diabetic and non-diabetic instances (stratified split).

Model Training: The SVM model is created using the `SVC` class from the `sklearn.svm` module with a linear kernel. The linear kernel creates a decision boundary that is a linear combination of the input features. The model is trained using the training data (X_train and Y_train) using the `fit` method.

Graphical User Interface (GUI): The GUI is created using the Tkinter library, which provides tools for building graphical user interfaces. The window is created using the `Tk` class from Tkinter.

Input Fields: The input fields are created using the `Entry` class from Tkinter. Each input field corresponds to a feature in the diabetes dataset. The user can enter values for pregnancies, glucose level, blood pressure, skin thickness, insulin level, BMI, diabetes pedigree, and age.

Test Button: The "Test" button is created using the `Button` class from Tkinter. It is associated with the `test_diabetes` function, which is called when the button is clicked.

Prediction: When the "Test" button is clicked, the `test_diabetes` function is executed. It retrieves the values entered by the user from the input fields. The input values are converted into a numpy array using `np.asarray` and reshaped to match the expected input shape for prediction. The input data is standardized using the `transform` method of the scaler that was fitted earlier. The SVM model then predicts the outcome (diabetic or not diabetic) based on the standardized input data using the `predict` method.

Result Display: The prediction result is displayed in a label using the `Label` class from Tkinter. The label's text is updated to indicate whether the person is diabetic or not based on the model's prediction.

Reset Button: The "Reset" button is created using the `Button` class from Tkinter. When clicked, it calls the `reset_inputs` function, which clears all the input fields and removes the prediction result from the label.

Overall, the project utilizes pandas for data loading and manipulation, scikit-learn for model training and evaluation, and Tkinter for building the graphical user interface. The SVM model is used to learn the patterns in the training data and make predictions on new input data provided by the user through the GUI.
