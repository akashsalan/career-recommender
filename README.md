# 🎓 Career Recommender API

A **Flask-based Machine Learning API** that predicts suitable career options for students based on their **stream, best subject, and interest**.

The model is trained live at startup using a **Decision Tree Classifier** and supports **CORS** for frontend integration.

---

## 🚀 Features
- 🔍 Predicts student career paths using Machine Learning
- 🌐 REST API built with Flask
- 📊 Uses a CSV dataset for training
- 🧠 Decision Tree model trained at runtime
- 🔄 Label encoding handled automatically
- 🌍 CORS enabled for frontend apps
- ⚡ Fast JSON-based predictions
---

## 🧠 Tech Stack
- Python 3.8+
- Flask
- Flask-CORS
- Pandas
- Scikit-learn
---

## 📦 Installation
### 1. Clone the Repository
git clone https://github.com/yourusername/career-recommender-api.git
cd career-recommender-api
### 2. Create a Virtual Environment (Optional but Recommended)
bash 
python -m venv venv 
source venv/bin/activate # On Windows: venv\Scripts\activate 
### 3. Install Dependencies
bash 
pip install flask flask-cors pandas scikit-learn 
---
### 📂 Project Structure
directory structure:
|-- career-recommender-api/
|   |-- app.py
|   |-- student_career_351_final_fixed.csv
|   |-- README.md
|   |-- requirements.txt 
---
### ▶️ Running the Application
def run the server:
bash 
python app.py 
the server will start at:
http://localhost:5000 
---
## 🌐 API Endpoints
### 🔹 Home Route GET /
Returns a status message.
txt:
"Career Recommender API is running (CORS enabled, model trained live)."
### 🔹 Predict Career POST /predict
Predicts a career based on student details.
#### 📥 Request Body (JSON)
jason:
{
"stream": "Science",
"best_subject": "Maths",
"interest": "Technology"
}
default response:
ejson:
{
"career": "Software Engineer"
}
eerror response:
ejson:
{
"error": "Input value not found in training data"
}
details:
a) Input values must exist in the dataset.
b) Model is trained every time the server starts.
c) Label encoding is handled automatically.
d) Input formatting is normalized using .title()
details about customization ideas and license are also included.
