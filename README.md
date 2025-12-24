# Medico Bot

A healthcare chatbot that predicts potential diseases based on user-reported symptoms using machine learning. This project aims to provide preliminary health assessments and guidance, but it is not a substitute for professional medical advice.

## Features

- **Disease Prediction**: Uses a Decision Tree Classifier trained on symptom data to predict possible diseases.
- **Symptom Severity Calculation**: Calculates the severity of symptoms based on duration and individual symptom weights.
- **Web Interface**: Interactive web application built with Gradio for easy user interaction.
- **Text-to-Speech**: Integrated text-to-speech functionality for accessibility.
- **Fuzzy Matching**: Handles slight variations in symptom input using fuzzy string matching.
- **Medical Information**: Provides disease descriptions and precautionary measures.
- **Multiple Interfaces**: Includes command-line, notebook-based, and web-based implementations.

## Technologies Used

- **Python**: Core programming language
- **Machine Learning**:
  - scikit-learn (Decision Tree Classifier)
  - pandas and numpy for data manipulation
- **Web Framework**: Gradio for web interface
- **Text-to-Speech**: pyttsx3
- **Fuzzy Matching**: fuzzywuzzy
- **Data Processing**: CSV files for datasets

## Datasets

The project uses the following datasets (included in the project directory):

- `Training.csv`: Training data with symptoms and corresponding diseases
- `Testing.csv`: Testing data for model evaluation
- `symptom_Description.csv`: Descriptions of various diseases
- `symptom_precaution.csv`: Precautionary measures for diseases
- `Symptom_severity.csv`: Severity scores for individual symptoms

## Installation

1. Clone the repository:
   ```bash
   git clone <repository-url>
   cd medico-bot
   ```

2. Create a virtual environment (recommended):
   ```bash
   python -m venv venv
   source venv/bin/activate  # On Windows: venv\Scripts\activate
   ```

3. Install required Python packages:
   ```bash
   pip install -r requirements.txt
   ```

   Or install individually:
   ```bash
   pip install pandas numpy scikit-learn gradio pyttsx3 fuzzywuzzy
   ```

### Requirements File

Create a `requirements.txt` file with the following content:

```
pandas
numpy
scikit-learn
gradio
pyttsx3
fuzzywuzzy
```

## Usage

### Web Interface (Recommended)

Run the Gradio web application:

```python
python app.py  # Assuming you have a main app.py file
```

Or run directly from a notebook cell:

```python
interface.launch()
```

Access the web interface at the provided local URL.

### Jupyter Notebook

Open and run the provided Jupyter notebooks:

- `medical bot.ipynb`: Main implementation with text-to-speech
- `medico.ipynb`: Alternative implementation
- `Output interface.ipynb`: Web interface implementations

### Command Line

For command-line usage, refer to the notebook implementations and adapt the code accordingly.

## Input Format

- **Name**: User's name (optional)
- **Symptoms**: Comma-separated list of symptoms (e.g., "fever, cough, headache")
- **Duration**: Number of days symptoms have been present
- **Medical History**: Optional previous medical conditions

## Output

The chatbot provides:

- Predicted disease
- Disease description
- Recommended precautions
- Severity assessment
- Advice on seeking professional medical help

## Model Training

The Decision Tree Classifier is trained on the provided training data. To retrain or modify:

1. Load the training data
2. Preprocess features and labels
3. Train the model
4. Evaluate on test data

## Limitations

- This tool provides preliminary predictions only
- Always consult healthcare professionals for accurate diagnosis
- Model accuracy depends on the quality and completeness of input symptoms
- Not suitable for emergency medical situations

## Contributing

1. Fork the repository
2. Create a feature branch
3. Make your changes
4. Submit a pull request

## Disclaimer

This project is for educational and informational purposes only. It should not be used as a substitute for professional medical advice, diagnosis, or treatment. Always seek the advice of qualified health providers with questions about medical conditions.

## Future Improvements

- Integration with larger medical databases
- Support for multiple languages
- Enhanced user authentication and data privacy
- Integration with telemedicine platforms
- Improved model accuracy with more diverse datasets

