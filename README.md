Star Classification

This project is a machine learning study aimed at classifying celestial objects (Stars, Galaxies, Quasars) using spectral data provided by the Sloan Digital Sky Survey (SDSS). The performance of different algorithms (k-NN, Naive Bayes, Random Forest) is compared to identify the most effective model.

About the Project

The dataset contains 100,000 astronomical observations along with their photometric features. The goal of the project is to predict the class of a celestial object based on these physical properties.

Target Classes:
	•	GALAXY: Galaxies
	•	STAR: Stars
	•	QSO: Quasars

📂 Dataset and Features

Dataset Used: star_classification.csv

Key features used for model training:
	•	u, g, r, i, z: Light intensity values obtained from filters at different wavelengths.
	•	redshift: A critical value indicating the object’s recession velocity and its position in the universe.
	•	Note: Identifier fields such as obj_ID and run_ID, which have no physical meaning, are removed from the dataset.

Methods Applied

1. Data Preprocessing
	•	Encoding: The categorical target variable (class) is converted into numerical form (0, 1, 2) using LabelEncoder.
	•	Scaling: StandardScaler is applied to eliminate scale differences between features. This step is especially critical for the performance of the k-NN algorithm.

2. Models and Comparison

Three different classification algorithms are trained and evaluated:
	1.	k-Nearest Neighbors (k-NN):
	•	Parameters: n_neighbors=5, weights='distance'
	•	Result: Achieved high accuracy (94%+) thanks to its distance-weighted structure.
	2.	Naive Bayes (GaussianNB):
	•	Result: Showed lower performance (around 74%) compared to other models due to the complexity of the data distribution.
	3.	Random Forest Classifier:
	•	Result: Provided the highest performance by leveraging an ensemble of decision trees, effectively capturing complex relationships in the dataset.

Results

Based on accuracy scores and confusion matrix analysis:
	•	Random Forest is the most successful model in terms of both overall accuracy and distinguishing rare classes (e.g., Quasars).
	•	The redshift feature stands out as one of the most discriminative features for classification.
