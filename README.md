# Facial Emotion Classification

This project demonstrates how to build and train a facial emotion classification model using transfer learning with a pre-trained EfficientNetV2S model. The model is trained to classify images into three emotions: Happy, Neutral, and Sad.

## Dataset

The dataset used for this project is the [Facial Emotion Dataset](https://www.kaggle.com/datasets/himanshuydv11/facial-emotion-dataset) from Kaggle. The project focuses on the 'Happy', 'Neutral', and 'Sad' classes.

## Project Structure

The notebook performs the following steps:

1.  **Setup:** Installs necessary libraries and downloads the dataset from Kaggle.
2.  **Data Preparation:** Unzips the dataset, organizes the relevant emotion classes into a new directory (`data_fix`), and prepares the data using `ImageDataGenerator` for training and validation.
3.  **Model Building:** Loads a pre-trained EfficientNetV2S model (without the top classification layer) and adds new layers for the facial emotion classification task.
4.  **Model Training:** Compiles and trains the model using the prepared data, with a callback to stop training early if desired accuracy is reached.
5.  **Model Conversion (Optional):** (Not explicitly in the provided code, but a potential next step) Convert the trained model to TensorFlow Lite for deployment.

## Requirements

*   Python 3
*   TensorFlow
*   Keras
*   Pandas
*   Numpy
*   Matplotlib
*   Kaggle (with `kaggle.json` configured)

## Setup and Running

1.  **Clone the repository (if applicable) or open the Colab notebook.**
2.  **Install dependencies:** Ensure you have the required libraries installed. If using the Colab notebook, the first few cells handle this.
3.  **Download the dataset:** Follow the steps in the notebook to download the dataset from Kaggle. You will need a Kaggle account and API key (`kaggle.json`).
4.  **Run the notebook cells sequentially.** The notebook will handle data preparation, model training, and evaluation.

## Results

The training process outputs the accuracy and loss for both the training and validation datasets, allowing you to monitor the model's performance.

## Future Work

*   Include all emotion classes from the dataset.
*   Implement more advanced data augmentation techniques.
*   Explore other pre-trained models for transfer learning.
*   Convert the model to TensorFlow Lite and deploy it on a mobile or edge device.
*   Add a section for making predictions on new images.
