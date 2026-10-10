# LSTM and GRU End-to-End Deep Learning Project: Predicting Next Word

This project demonstrates a text generation / next-word prediction pipeline using recurrent neural networks. It trains and loads a model that predicts the most likely next word given a sequence of preceding words, then exposes the result through a Streamlit web app.

## Overview

The project uses text from Shakespeare's Hamlet as the corpus and builds a sequence-based language model using an LSTM architecture. The trained model is then loaded from disk and used to predict the next word in a user-provided sentence.

This repository includes:
- a trained Keras model (`next_word.h5`)
- a saved tokenizer (`tokenizere.pickle`)
- a Streamlit app (`main.py`)
- text data (`hamlet.txt`)
- dependency list (`requirements.txt`)

## Project Goals

- Build an end-to-end text prediction model
- Convert text into token sequences
- Use sequence padding for fixed-length model input
- Train a recurrent neural network for next-word prediction
- Deploy the model in a user-friendly interface with Streamlit

## Tech Stack

- Python
- TensorFlow / Keras
- NumPy
- Streamlit
- scikit-learn
- Pandas
- NLTK
- Matplotlib
- TensorBoard

## Repository Structure

```text
.
├── main.py                  # Streamlit app for prediction UI
├── hamlet.txt               # Training corpus
├── next_word.h5             # Trained model artifact
├── tokenizere.pickle        # Saved tokenizer
├── requirements.txt         # Python dependencies
├── .streamlit/
│   └── config.toml         # Streamlit configuration
├── given_code/              # Reference or supplementary code
├── experieemnts.ipynb       # Exploration notebook
└── README.md                # Project documentation
```

## Setup

1. Clone the repository.
2. Open a terminal in the project directory.
3. Create and activate a virtual environment if desired.
4. Install the required dependencies:

```bash
pip install -r requirements.txt
```

## Run the Application

Start the Streamlit app with:

```bash
streamlit run main.py
```

Then open the local URL shown in the terminal (typically `http://localhost:8501`).

## How It Works

1. The app loads the saved tokenizer and trained model.
2. User input is converted into token IDs.
3. The text is trimmed or padded to match the model input length.
4. The model predicts the next word from the input sequence.
5. The result is displayed in the UI.

## Example Inputs

- `To be or not to`
- `Something is rotten`
- `The rest is silence`

## Notes

- The model is pre-trained and saved in the repository, so you do not need to retrain it to run the app.
- The project is intended as a practical learning exercise for sequence modeling and next-word prediction with neural networks.
- The `given_code` directory contains additional example code and experiments that can be useful for reference.

## License

This project is provided as a learning/demo project. Add an appropriate license if you plan to share or publish it publicly.

## Future Improvements

- Train on a larger corpus
- Add top-k prediction alternatives
- Support sentence continuation and text generation
- Improve model accuracy with GRU/LSTM tuning
- Add deployment support for a production API or web service
