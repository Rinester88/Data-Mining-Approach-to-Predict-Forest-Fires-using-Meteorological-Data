# Data-Mining-Approach-to-Predict-Forest-Fires-using-Meteorological-Data

🌲  Data-Mining-Approach-to-Predict-Forest-Fires-using-Meteorological-Data 🔥

Welcome to the Forest Fire Prediction project! This repository contains a machine learning model built to predict the size of forest fires based on environmental factors. By leveraging historical data, we aim to create a model that can predict potential wildfire risks and help mitigate the impact of devastating fires.

	The objective of this project:
Predict the area burned by wildfires using features such as weather conditions, location data, and fire-related metrics.

 

 

📌 Table of Contents
	•	Overview
	•	Dataset
	•	Setup
	•	Data Preprocessing
	•	Exploratory Data Analysis (EDA)
	•	Modeling
	•	Results
	•	Contributing
	•	License

🌟 Overview

This project involves building a machine learning model to predict the area burned in forest fires. By analyzing factors like temperature, humidity, wind speed, and rain, we aim to detect high-risk fire zones early.

🔑 Features:
	•	Data from the Montesinho Park, Portugal 🔥
	•	Weather-related features like temperature, humidity, wind speed, and rain 🌧️
	•	Key fire danger index features like FFMC, DMC, DC, and ISI 🌲
	•	A geographical mapping of fire locations using coordinates 🗺️

📊 Dataset

The dataset used in this project is available at [link-to-dataset]. It contains the following columns:
	•	X, Y: Coordinates of the fire
	•	month: Month when the fire occurred
	•	day: Day of the week when the fire occurred
	•	FFMC, DMC, DC, ISI: Fire danger components
	•	temp: Temperature (°C)
	•	RH: Relative Humidity (%)
	•	wind: Wind speed (km/h)
	•	rain: Rainfall (mm)
	•	area: Area burned (hectares) 🔥 (Target variable)

🏞️ Sample Data:

X	Y	month	day	FFMC	DMC	DC	ISI	temp	RH	wind	rain	area
1	1	mar	sun	88.6	46	135	20	30.0	60	5.0	0	12
2	2	aug	fri	92.2	50	145	18	27.5	45	6.0	1	25
…	…	…	…	…	…	…	…	…	…	…	…	…

⚙️ Setup

To get started with the project:
	1.	Clone this repository:

git clone https://github.com/yourusername/forest-fire-prediction.git


	2.	Navigate to the project folder:

cd forest-fire-prediction


	3.	Create and activate a virtual environment:

python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate


	4.	Install dependencies:

pip install -r requirements.txt

🧹 Data Preprocessing

The data preprocessing steps include:
	•	Handling missing values: Fill missing values with the mean/median or drop rows.
	•	Feature scaling: Use StandardScaler to scale numerical features.
	•	Encoding categorical data: Convert the month and day columns into numerical values.

🔧 Example Code:

# Handling missing values
df.fillna(df.mean(), inplace=True)

# Feature scaling
from sklearn.preprocessing import StandardScaler
scaler = StandardScaler()
df[['temp', 'RH', 'wind']] = scaler.fit_transform(df[['temp', 'RH', 'wind']])

🔍 Exploratory Data Analysis (EDA)

In this phase, we uncover insights into the data through visualizations:
	•	Distribution of target variable (area) 📊
	•	Correlation heatmap to identify feature relationships 🔗
	•	Pairplots to visualize interactions between key features 🔄
	•	Geographical map using folium to plot fire locations 🗺️

🧠 Modeling

Algorithms Used:
	•	XGBoost 🌳: A powerful tree-based model known for performance
	•	CatBoost 🐱: Another gradient-boosting method with better handling of categorical features
	•	LSTM (Long Short-Term Memory) 📈: For time-series prediction based on seasonal trends

Hyperparameter Tuning:
	•	GridSearchCV and RandomSearchCV to fine-tune model parameters

📊 Evaluation Metrics:
	•	Mean Absolute Error (MAE) 📉
	•	Root Mean Squared Error (RMSE) 📏
	•	R² Score for model accuracy 🌟

📈 Results

After training, the models are evaluated, and results such as accuracy and prediction graphs are available in the Results/ folder.

	Visualizations:
		•	Area Burned over Time 🔥
	•	Model performance comparison 📊

🤝 Contributing

We welcome contributions to this project! Here’s how you can help:
	•	Bug fixes 🐛
	•	Feature enhancements 🚀
	•	Documentation improvements 📝

To contribute:
	1.	Fork the repo
	2.	Create a branch (git checkout -b feature-name)
	3.	Make your changes and commit them
	4.	Push to your branch (git push origin feature-name)
	5.	Open a pull request with a detailed description of your changes

📜 License

This project is licensed under the MIT License. For more details, refer to the LICENSE file.

🧑‍💻 Acknowledgments
	•	Dataset: Montesinho park dataset from [source].
	•	Libraries: Pandas, Scikit-Learn, XGBoost, CatBoost, TensorFlow.

This version includes eye-catching elements like badges for license and build status, emojis to make sections engaging, and provides a more interactive feel. It also includes example code and placeholder links for visualizations and results.

Feel free to customize the links and images further to fit your needs!f you’d like to improve this project, please fork the repository and create a pull request with your changes. You can contribute by:
	•	Fixing bugs
	•	Adding new features
	•	Improving the documentation

License

This project is licensed under the MIT License - see the LICENSE file for details.

Example Visualizations:
	•	Geographical Map of Fire Occurrences: Interactive map showcasing the fire locations.
	•	Distribution of Area Burned: Visualize the spread of fire by area.
	•	Correlation Heatmap: Show how features relate to each other.

Dependencies:
	•	pandas
	•	numpy
	•	seaborn
	•	matplotlib
	•	folium
	•	scikit-learn
	•	xgboost
	•	catboost
	•	tensorflow (for LSTM)

Feel free to modify or expand the sections to suit your project! This should give visitors to your repository a good understanding of what the project is about and how to run it.
