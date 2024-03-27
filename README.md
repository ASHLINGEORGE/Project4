# AI-Based Road Cleanliness Assessment System using Image  Classification
![AI](images/intro.jpg)
This project aims to classify images of roads as either clean or cluttered using machine learning techniques. The classification is performed using Support Vector Machine (SVM) and Convolutional Neural Network (CNN) models trained on a dataset of road images.

## Features

- [Introduction](#introduction)
- [Data Collection](#data-collection)
- [Data Preprocessing and Loading](#data-preprocessing-and-loading)
- [Model Training](#model-training)
- [Evaluation and Visualization](#evaluation-and-visualization)
- [Gradio Interface](#gradio-interface)
- [Usage](#usage)
- [Dependencies](#dependencies)
- [License](#license)


### Introduction

Road cleanliness is a crucial aspect of public safety and environmental sustainability. This project addresses the problem of identifying whether a road is clean or cluttered based on image data. By deploying machine learning models, we aim to automate this classification process and provide insights for road maintenance and cleanliness efforts.

### Data Collection

Images of both clean and cluttered roads were collected from various sources, ensuring diversity in scenarios, lighting conditions, and environments. Ethical considerations were followed to respect copyright laws and obtain necessary permissions for image usage.

### Data Preprocessing and Loading

Collected images were preprocessed by resizing for uniformity and applying noise reduction techniques to enhance quality. The preprocessed images were then loaded into a database, categorizing them as clean or cluttered roads, for easy access during model training.

### Model Training

Support Vector Machine (SVM) and Convolutional Neural Network (CNN) models were trained on the preprocessed image data. Hyperparameter tuning was performed for the SVM model using GridSearchCV to optimize performance. The CNN model was trained on TensorFlow/Keras with a defined architecture comprising convolutional, pooling, and fully connected layers.

## Optimization:

- Initially, the model was trained and tested using Support Vector Machines (SVM), but the obtained accuracy did not meet the desired level of performance. 
- Consequently, the model underwent optimization using Convolutional Neural Networks (CNN), a process that resulted in a remarkable enhancement, pushing the accuracy metric to an impressive 94%.

### Evaluation and Visualization

Model performance was evaluated using metrics such as accuracy, precision, recall, and F1-score to assess clean and cluttered road classification. Training and validation loss/accuracy were visualized using Matplotlib to monitor model learning progress.

### Gradio Interface

A Gradio interface was developed for the CNN model, enabling real-time interaction. Users can upload images to receive predictions on road cleanliness without requiring expertise in coding or machine learning.

## File Structure Description:

- `ETL.ipynb`: Jupyter Notebook containing the Extraction, Transformation, and Loading (ETL) process for the project. This notebook handles the extraction of data, processing of data, and loading of data into the database.

- `Model.ipynb`: Python Notebook containing the retrieval of data from the database, splitting of training and testing data, tuning of the model (SVM), optimization of the model (CNN), and deployment of the model. This notebook covers the entire modeling pipeline for the project.

- `clean_cluttered_road.db`: SQLite database file containing the cleaned and preprocessed data for the project.

- `data/image_data`: Directory containing all the image data to be fed to the database. This directory stores the raw image files used in the project.

- `images`: Directory containing images related to the project. This directory may include visualizations, graphs, or other images used in the project documentation or README.

- `power-point`: Directory containing the PowerPoint file(s) related to the project. This directory may include presentations, slides, or other PowerPoint files.

- `README.md`: This file, providing an overview of the repository, project description, file structure, and usage instructions.

## Usage:
1. Run the `ETL.ipynb` file to save the SQLite database to your local machine as `clean_cluttered_road.db`. 

2. Once the database is saved locally, ensure to back up the `clean_cluttered_road.db` file to  Google Drive.

3. Open the `Model.ipynb` notebook in Google Colab. Connect the notebook to your Google Drive by following these steps:
    - Mount your Google Drive by executing the provided code snippet in the notebook. This will allow access to files stored in your Google Drive.
    - Navigate to the directory where `clean_cluttered_road.db` is saved in your Google Drive and copy the path to the respective variable.

4. Proceed with the execution of the `Model.ipynb` notebook. This notebook contains the retrieval of data from the database, splitting of training and testing data, tuning of the model (SVM), optimization of the model (CNN), and deployment of the model. It covers the entire modeling pipeline for the project.

## Author

- ASHLIN SHINU GEORGE

