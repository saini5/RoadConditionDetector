# Detecting Road Conditions Using Smartphone Sensors#

##Problem Statement##
Design and Develop a technique for detecting road anomalies using smartphone sensors where road anomalies include bump, pothole,brake and rough road.

##Steps Involved##
1. Data Collection
 1. We'll be developing our own app for collecting the data (will be complete within 10 days i.e. till 27th January,2015). 
 2. The data collected from the app will be processed using some filters like the Butterworth low-pass filter for expanding the number of features and compacting the number of samples for the reading window corresponding to one classification.
2. Data Cleaning
 1. We'll be cleaning the data using R programming language.
 2. For a specific format of the raw data collected from smartphones, we have already developed a sub-project in R to clean the data. The specific format of raw data(and the actual raw dataset as well) from smartphones can be found at [UCI Repository](http://archive.ics.uci.edu/ml/datasets/Human+Activity+Recognition+Using+Smartphones) and our sub-project for cleaning this data can be found on [my github repository](http://archive.ics.uci.edu/ml/datasets/Human+Activity+Recognition+Using+Smartphones) (look for the file run_analysis.R).
 3. **Note:** The main aim for the *app of data collection* in step 1.1 is to create a dataset similar in format to the *one available on UCI link above* and with the exhaustive set of features *directly* and *derived through the application of certain filters* from the accelerometers as well for better classification. The data thus gathered by the app will be cleaned by a slightly modified version of the step 2.2 R sub-project.
3. Exploratory Data Analysis and Machine Learning
 1. After cleaning the data, we'll analyze the tidy data set so as to select a sub-set of Machine Learning techniques to be applied.
 2. Applying specific ML techniques chosen in Step 3.1 
4. Evaluating the Machine Learning System
 1. Each technique applied above will be evaluated against cross-validation data sets and test data sets which are too collected by the app in Step 1.1
 2. The best ML technique chosen from the above evaluation will be applied to learn the classification of potholes, bumps, etc and can be used further for prediction purposes.

##Scope##
1. A specific app will be developed for collecting the data which involves active participation of the smartphone user to classify manually whether the smartphone just went through a bump, pothole, braking, etc events. Hence, the data collection part is not crowd-sourced as of now(in the sense that it doesn't collect data in the background, but involves active participation of the user).
2. As a final result, the machine learning system would be able to classify new readings from the smartphones. But still, it is uncertain that we will be able to make a final app with real-time classification and color-coding on the maps. But what we will be able to complete is that *collect a new reading using a seperate data collecting app*(which will support crowdsourcing and run in the background with no active participation of the user(i.e. no manual interaction for collection; the app will collect data silently) ), *the reading will be transferred to a computer* (may be through background uploading on our server), *where some pre-processing(1.2) and data cleaning(2) will be done* and *will predict what it is(a pothole, or something else) using the parameters(or weights) initially determined by the ML system on the training data set*.
3. The server can then in future color, code that region(identfied by lat and long) on the map accordingly(based on the reading shown by maximum users on that particular spot on map) which would be available to all users to see.

Contents of mail apart from this: 
1. This project can be followed on [RoadConditionDetector repo](https://github.com/qubit93/RoadConditionDetector.git).
2. 
