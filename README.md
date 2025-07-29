# Fake Currency Detection System

This project is a deep learning-based web application for detecting counterfeit Indian currency notes using ResNet50 and Streamlit. Users can upload an image of a currency note, select the denomination, and receive a real-time classification (Real or Fake) along with confidence scores. The system is designed for ease of use and can assist in quick verification of currency authenticity.

---

## Features

- Upload images of ₹50, ₹100, ₹500, or ₹2000 currency notes
- Real-time prediction of note authenticity (Real or Fake)
- Pretrained CNN models based on ResNet50 for each denomination
- Toggle between dark and light mode in the user interface
- Keeps track of prediction history during the session
- Provides safety instructions if a fake note is detected

---

## Technology Stack

- Python
- Streamlit
- TensorFlow / Keras
- ResNet50 (Transfer Learning)
- PIL & NumPy for image preprocessing

---

## Project Structure

```
.
├── app.py                      # Main Streamlit application
├── 50rs_Identification.ipynb   # Model training notebook for ₹50 notes
├── 100rs_Identification.ipynb  # Model training notebook for ₹100 notes
├── 500rs_Identification.ipynb  # Model training notebook for ₹500 notes
├── 2000rs_Identification.ipynb # Model training notebook for ₹2000 notes
├── model_50rs.keras            # Trained model for ₹50 notes
├── model_100rs.keras           # Trained model for ₹100 notes
├── model_500rs.keras           # Trained model for ₹500 notes
├── model_2000rs.keras          # Trained model for ₹2000 notes
```

---

## How to Run

### Prerequisites

Ensure the following are installed:

- Python 3.7 or higher
- Required Python libraries:
  - streamlit
  - tensorflow
  - pillow
  - numpy

### Running the Application

1. Clone the repository or download the project files.
2. Open your terminal or command prompt.
3. Navigate to the project directory.
4. Run the following command:

```
streamlit run app.py
```

5. Open the provided local URL (usually `http://localhost:8501`) in your browser.

---

## How It Works

1. Upload an image of an Indian currency note.
2. Select the denomination (₹50, ₹100, ₹500, or ₹2000).
3. The image is preprocessed (resized and normalized).
4. The pretrained ResNet50 model for that denomination is loaded.
5. The model classifies the note as Real or Fake with a confidence score.
6. If the note is fake, safety guidelines are shown to the user.

---

## Notes

- For accurate predictions, use clear, high-resolution images with good lighting.
- This system is trained on a custom dataset and may have limitations in handling damaged or highly varied counterfeit notes.

---

## License

This project is intended for educational and research purposes only. It is not certified for use in commercial or governmental counterfeit detection workflows.
