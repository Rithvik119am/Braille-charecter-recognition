# Braille Image to Telugu Converter

This project is a web application that converts images of Braille characters into their corresponding Telugu characters. It uses a deep learning model to perform the character recognition and provides a user-friendly interface built with Streamlit.

## How it Works

The application is built using Streamlit and has two main pages:
*   **Home:** Provides an introduction to Braille, Bharati Braille, and Telugu Braille.
*   **Predict:** Allows users to upload an image of a Braille character.

The prediction process involves these steps:
1.  The uploaded image is read and decoded.
2.  The image is resized to 28x28 pixels.
3.  Pixel values are normalized (divided by 255.0).
4.  The pre-trained Keras model (`custom_model.h5`) predicts the character.
5.  The model's numerical output is mapped to the corresponding Telugu character.

## Installation

1.  **Clone the repository:**
    ```bash
    git clone https://github.com/Rithvik119am/Braille-charecter-recognition
    cd Braille-charecter-recognition
    ```
2.  **Create and activate a virtual environment (recommended):**
    ```bash
    python -m venv venv
    source venv/bin/activate  # On Windows use `venv\Scripts\activate`
    ```
3.  **Install the dependencies:**
    Make sure you have Python 3.8 or newer.
    ```bash
    pip install -r installed_packages.txt
    ```

## Usage

1.  **Run the Streamlit application:**
    ```bash
    streamlit run app.py
    ```
2.  Open your web browser and navigate to the local URL provided by Streamlit (usually `http://localhost:8501`).
3.  **Navigate to the "Predict" page** using the sidebar.
4.  **Upload an image** of a Braille character (e.g., a `.jpg` file).
5.  The application will display the predicted Telugu character.

## Model

The character recognition is performed by a pre-trained Convolutional Neural Network (CNN).
*   The model is saved in the `custom_model.h5` file.
*   It was built using Keras with a TensorFlow backend.
*   The architecture includes convolutional layers, max pooling, dropout for regularization, and dense layers for classification.
*   The notebook `braille-character-recognition.ipynb` contains the details of the model's architecture, training process, and evaluation.

## Files

*   `app.py`: The main Streamlit application script.
*   `custom_model.h5`: The pre-trained Keras model for Braille to Telugu character recognition.
*   `braille-character-recognition.ipynb`: Jupyter Notebook containing the model development process (data loading, preprocessing, model architecture, training, and evaluation).
*   `installed_packages.txt`: A list of Python packages required to run the project.
*   `home_image.jpg`: Image displayed on the Home page of the Streamlit app.
*   `info.jpg`: Image providing information on Braille to Telugu character mapping, displayed on the Home page.
*   `uploaded_image.jpg`: Placeholder or example of an image that can be uploaded for prediction (actual uploaded images are handled by the app).
*   `README.md`: This file, providing an overview and instructions for the project.
