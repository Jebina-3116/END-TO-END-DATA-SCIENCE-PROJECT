# END-TO-END-DATA-SCIENCE-PROJECT
COMPANY:CODTECH IT SOLUTIONS

NAME:JEBINA SELIN S.D

INTERN ID:CT04DG3456

DOMAIN:DATA SCIENCE

DURATION:4 WEEKS
INTRODUCTION:
The goal of the project was to predict house prices using real-world housing data, train a suitable machine learning model, and deploy the trained model via a RESTful API using Flask. This project served as a practical exposure to the full lifecycle of a data science application—from data collection and preprocessing to model deployment and testing.

 Data Collection and Preprocessing
The dataset used for this project was the California Housing dataset, a popular dataset available within the scikit-learn library. This dataset contains various features related to housing demographics and geographic data in California, including:

Median income (MedInc)

House age (HouseAge)

Average number of rooms (AveRooms)

Average number of bedrooms (AveBedrms)

Population

Average occupancy (AveOccup)

Latitude

Longitude

Using Pandas, the data was converted into a DataFrame for better handling. The target variable, which represents the median house value, was added to the DataFrame. The data was then split into training and testing sets using an 80-20 ratio via train_test_split to evaluate model performance objectively.

 Model Training
I selected the Linear Regression algorithm for this regression problem due to its simplicity and interpretability. Using scikit-learn’s LinearRegression model, I trained the model on the training dataset. After training, the model could take new input data and predict the expected house price. The trained model was then serialized using Python’s pickle module and saved as model.pkl. This allowed me to reuse the model for real-time predictions without retraining.

 API Development and Deployment
To make the model accessible, I created a Flask-based REST API with two endpoints:

Home Route (/)
A basic GET route that returns a confirmation message: “🏠 House Price Prediction API is Running!”

Prediction Route (/predict)
A POST route that accepts JSON data containing values for the 8 input features. It reshapes the input into a NumPy array, makes a prediction using the trained model, and returns the predicted price in JSON format.

Here is an example input JSON sent to the /predict endpoint:

json
Copy
Edit
{
  "MedInc": 8.3,
  "HouseAge": 25.0,
  "AveRooms": 6.0,
  "AveBedrms": 1.0,
  "Population": 1000,
  "AveOccup": 3.5,
  "Latitude": 34.0,
  "Longitude": -118.0
}
The API response returns the predicted price:

json
Copy
Edit
{
  "predicted_price": 3.28
}
Testing was performed using Python’s requests module, which allowed simulation of API calls directly from a script, ensuring the server was responding with accurate predictions.

 Learning Outcomes
This internship project helped me strengthen my knowledge and skills in the following areas:

Understanding data preprocessing and regression modeling techniques.

Using machine learning libraries like Scikit-learn to build models.

Working with Flask to develop and deploy APIs.

Serializing models using Pickle for deployment.

Using RESTful architecture for client-server communication.

Testing APIs using Python scripts and JSON data.

 Conclusion
Through this project, I gained a comprehensive understanding of how data science models are not just trained but also deployed and consumed in real-time applications. This experience has given me a strong foundation in model deployment, API development, and full-stack machine learning systems, which are crucial for real-world AI/ML jobs. It also emphasized the importance of clean code, organized architecture, and usability in developing production-ready applications. I am grateful to CodTech for providing this opportunity and look forward to applying these skills in future projects.

OUTPUT:
<img width="657" height="753" alt="pic" src="https://github.com/user-attachments/assets/03c9c2b1-1bda-4fae-b671-2d4dfb698127" />
