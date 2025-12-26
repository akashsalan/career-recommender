\# 🎓 Career Recommender API

A \*\*Flask-based Machine Learning API\*\* that predicts suitable career options for students based on their \*\*stream, best subject, and interest\*\*.

The model is trained live at startup using a \*\*Decision Tree Classifier\*\* and supports \*\*CORS\*\* for frontend integration.

\---

\## 🚀 Features

\- 🔍 Predicts student career paths using Machine Learning

\- 🌐 REST API built with Flask

\- 📊 Uses a CSV dataset for training

\- 🧠 Decision Tree model trained at runtime

\- 🔄 Label encoding handled automatically

\- 🌍 CORS enabled for frontend apps

\- ⚡ Fast JSON-based predictions

\---

\## 🧠 Tech Stack

\- Python 3.8+

\- Flask

\- Flask-CORS

\- Pandas

\- Scikit-learn

\---

\## 📦 Installation

\### 1. Clone the Repository

\`\`\`bash

git clone https://github.com/yourusername/career-recommender-api.git

cd career-recommender-api

2\. Create a Virtual Environment (Optional but Recommended)

bash

Copy code

python -m venv venv

source venv/bin/activate # On Windows: venv\\Scripts\\activate

3\. Install Dependencies

bash

Copy code

pip install flask flask-cors pandas scikit-learn

📂 Project Structure

Copy code

career-recommender-api/

│

├── app.py

├── student\_career\_351\_final\_fixed.csv

├── README.md

└── requirements.txt

▶️ Running the Application

bash

Copy code

python app.py

The server will start at:

arduino

Copy code

http://localhost:5000

🌐 API Endpoints

🔹 Home Route

GET /

Returns a status message.

text

Copy code

Career Recommender API is running (CORS enabled, model trained live).

🔹 Predict Career

POST /predict

Predicts a career based on student details.

📥 Request Body (JSON)

json

Copy code

{

"stream": "Science",

"best\_subject": "Maths",

"interest": "Technology"

}

📤 Response (JSON)

json

Copy code

{

"career": "Software Engineer"

}

❌ Error Response

json

Copy code

{

"error": "Input value not found in training data"

}

⚠️ Important Notes

Input values must exist in the dataset

Model is trained every time the server starts

Label encoding is handled automatically

Input formatting is normalized using .title()

🛠 Customization Ideas

Save trained model using joblib

Add confidence/probability scores

Handle unseen categories gracefully

Convert API to FastAPI

Add authentication and logging

Deploy to cloud platforms (Render, Railway, Heroku)

📄 License

This project is licensed under the MIT License.
