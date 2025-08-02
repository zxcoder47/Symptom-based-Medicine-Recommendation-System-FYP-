# Medical Diagnosis System (MDS)

A Flask-based web application that predicts diseases based on user-reported symptoms using machine learning algorithms. The system provides comprehensive health recommendations including medications, diet plans, precautions, and workout routines.

## 🎯 Project Overview

This Medical Diagnosis System is designed to help users get preliminary health assessments by analyzing their symptoms. The application uses a trained Random Forest machine learning model to predict potential diseases and provides holistic health recommendations.

### Key Features

- **Symptom-based Disease Prediction**: Input symptoms and get disease predictions
- **Comprehensive Health Recommendations**:
  - Detailed disease descriptions
  - Medication suggestions
  - Dietary recommendations
  - Precautionary measures
  - Workout routines
- **User-friendly Web Interface**: Clean, responsive Bootstrap-based UI
- **Multiple Pages**: Home, About, Contact, and Developer information
- **Real-time Predictions**: Instant results upon symptom submission

## 🏗️ Project Structure

```text
fyp/
├── main.py                 # Main Flask application
├── mrs.ipynb              # Jupyter notebook (likely for model training)
├── README.md              # Project documentation
├── dataset/               # Training and reference data
│   ├── description.csv    # Disease descriptions
│   ├── diets.csv         # Diet recommendations
│   ├── medications.csv   # Medication data
│   ├── precautions_df.csv # Precautionary measures
│   ├── Symptom-severity.csv # Symptom severity data
│   ├── symtoms_df.csv    # Symptoms dataset
│   ├── Training.csv      # Training data
│   └── workout_df.csv    # Workout recommendations
├── models/               # Trained ML models
│   ├── rf_model.pkl     # Random Forest model
│   └── svc.pkl          # Support Vector Classifier model
├── static/              # Static assets
│   ├── img.png
│   ├── img1.jpeg
│   ├── img2.jpeg
│   ├── img3.jpeg
│   └── img4.jpg
├── templates/           # HTML templates
│   ├── index.html      # Main page
│   ├── about.html      # About page
│   ├── contact.html    # Contact page
│   └── developer.html  # Developer information
└── fyp/                # Virtual environment
    ├── Scripts/
    ├── Lib/
    └── Include/
```

## 🚀 Installation and Setup

### Prerequisites

- Python 3.8 or higher
- pip (Python package installer)

### Step 1: Clone the Repository

```bash
git clone <repository-url>
cd fyp
```

### Step 2: Create Virtual Environment

```bash
python -m venv fyp
```

### Step 3: Activate Virtual Environment

**Windows:**

```bash
fyp\Scripts\activate
```

**macOS/Linux:**

```bash
source fyp/bin/activate
```

### Step 4: Install Required Packages

```bash
pip install -r requirements.txt
```

Alternatively, install packages manually:

```bash
pip install flask numpy pandas scikit-learn pickle-mixin
```

### Step 5: Run the Application

```bash
python main.py
```

The application will be available at `http://localhost:5000`

## 📊 Dataset Information

The application uses several CSV datasets:

- **symtoms_df.csv**: Contains disease-symptom mappings (4,922 records)
- **description.csv**: Disease descriptions and explanations
- **medications.csv**: Recommended medications for each disease
- **diets.csv**: Dietary recommendations per disease
- **precautions_df.csv**: Precautionary measures for diseases
- **workout_df.csv**: Exercise routines for different conditions
- **Training.csv**: Training data for machine learning model
- **Symptom-severity.csv**: Symptom severity classifications

## 🤖 Machine Learning Model

The system uses a **Random Forest Classifier** trained on symptom data to predict diseases. The model:

- **Input**: 132 different symptoms (binary encoded)
- **Output**: One of 41 possible diseases
- **Accuracy**: Model performance details in `mrs.ipynb`

### Supported Diseases (41 total)

Including but not limited to:

- Fungal infection
- Allergy
- GERD
- Diabetes
- Hypertension
- Migraine
- Heart attack
- Tuberculosis
- Common Cold
- Pneumonia
- And 31 more...

### Supported Symptoms (132 total)

Common symptoms include:

- itching, skin_rash, continuous_sneezing
- joint_pain, stomach_pain, fatigue
- headache, fever, cough
- nausea, vomiting, dizziness
- And 122 more symptoms...

## 🌐 Web Interface

### Main Features

1. **Home Page (`/`)**:
   - Symptom input form
   - Disease prediction results
   - Health recommendations display

2. **Prediction API (`/predict`)**:
   - Accepts comma-separated symptoms
   - Returns disease prediction with recommendations

3. **Information Pages**:
   - `/about`: About the system
   - `/contact`: Contact information  
   - `/developer`: Developer details

### Usage Instructions

1. Navigate to the home page
2. Enter symptoms separated by commas (e.g., "fever, headache, cough")
3. Click submit to get predictions
4. View comprehensive health recommendations

## 🔧 API Usage

### Predict Disease

**Endpoint**: `POST /predict`

**Parameters**:

- `symptoms`: Comma-separated list of symptoms

**Example**:

```html
<form method="POST" action="/predict">
    <input name="symptoms" value="fever, headache, fatigue">
    <button type="submit">Predict</button>
</form>
```

## 🧪 Testing

To test the application:

1. Start the Flask server
2. Navigate to `http://localhost:5000`
3. Enter test symptoms like: "itching, skin_rash, fatigue"
4. Verify prediction results and recommendations

## 📁 File Descriptions

- **main.py**: Core Flask application with routes and prediction logic
- **mrs.ipynb**: Jupyter notebook for model development and training
- **rf_model.pkl**: Serialized Random Forest model
- **svc.pkl**: Alternative Support Vector Classifier model

## 🔮 Future Enhancements

- [ ] Add user authentication and history tracking
- [ ] Implement severity scoring for symptoms
- [ ] Add multi-language support
- [ ] Include more diseases and symptoms
- [ ] Add appointment booking system
- [ ] Implement doctor consultation features
- [ ] Add mobile application
- [ ] Include image-based diagnosis

## ⚠️ Disclaimer

**This application is for educational and informational purposes only. It should not be used as a substitute for professional medical advice, diagnosis, or treatment. Always consult with qualified healthcare providers for medical concerns.**

## 👨‍💻 Developer Information

This project was developed as a Final Year Project (FYP) demonstrating the application of machine learning in healthcare diagnostics.

### Technologies Used

- **Backend**: Flask (Python)
- **Frontend**: HTML, CSS, Bootstrap 5.3.1
- **Machine Learning**: scikit-learn, Random Forest
- **Data Processing**: pandas, numpy
- **Model Serialization**: pickle

## 📄 License

This project is developed for educational purposes. Please ensure proper attribution when using or modifying the code.

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch
3. Make your changes
4. Submit a pull request

## 📞 Support

For questions or support, please refer to the contact page in the application or reach out through the developer information section.

---

**Note**: Ensure all CSV files are properly placed in the `dataset/` directory and model files are in the `models/` directory before running the application.
