# Chest X-Ray Classification Project :hospital:

## :dart: Objective
The primary goal of this project was to develop an effective deep learning model capable of classifying radiography images, specifically focusing on detecting COVID-19 cases.

## :open_file_folder: Data Source
The dataset, sourced from Kaggle, included:
- 3616 COVID-19 positive cases
- 10,192 Normal cases
- 6012 Lung Opacity (Non-COVID lung infection) cases
- 1345 Viral Pneumonia images

## :brain: Model Selection
We selected DenseNet169 for its balance between complexity and efficiency, ideal for the limited data in medical imaging tasks. The model was adapted by removing its built-in feature extraction layers and integrating custom feature extraction techniques.

## :gear: Data Preparation
- **Libraries and Functions:** Used OpenCV for image processing, Pandas for data manipulation, and TensorFlow with Keras for machine learning.
- **Data Splitting:** 80% training, 10% validation, and 10% test sets.
- **Data Augmentation:** Employed Image Data Generators for horizontal flipping during training.

## :building_construction: Model Definition
- **Architecture:** DenseNet169 as the base model with a custom dense layer for classification.
- **Compilation:** Used the Adamax optimizer, categorical crossentropy loss, and accuracy metric.

## :control_knobs: Callbacks
- **MyCallback:** A custom callback class for dynamic learning rate adjustment and user interaction during training.

## :running_man: Model Training
Utilized defined model, callbacks, and data generators, displaying key metrics during training.

## :test_tube: Model Evaluation
Evaluated the model on training, validation, and test sets to assess loss and accuracy.

## :chart_with_upwards_trend: Prediction and Analysis
- **Prediction:** Generated predictions on the test set.
- **Confusion Matrix and Classification Report:** Included for in-depth analysis.

## :page_with_curl: Technical Summary
- **Architecture:** DenseNet169 (pre-trained) with a custom layer.
- **Optimizer:** Adamax, learning rate 0.001.
- **Loss Function:** Categorical Crossentropy.
- **Data Augmentation:** Horizontal flipping.
- **Callbacks:** Custom for dynamic learning rate and training control.
- **Training Parameters:** 100 epochs, batch size of 16.

## :memo: Notes
- Script designed for Kaggle environment.
- Achieved ~96.27% accuracy on the test set.
- Generated CSV files for further analysis.

## :checkered_flag: Conclusion
This script offers a robust framework for training a chest X-ray classification model, particularly effective for respiratory conditions. DenseNet169, coupled with custom features, results in high accuracy, demonstrating the project's success in leveraging advanced machine learning for medical imaging.
