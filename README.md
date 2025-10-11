# 🤖 Smart ATS – Resume Evaluator using Google Gemini Pro

An interactive **Streamlit application** that evaluates resumes against job descriptions using **Google Gemini Pro (LLM)**.  
This project simulates an **ATS (Applicant Tracking System)** to help candidates improve their resumes for competitive tech roles such as **Data Science, Software Engineering, and Machine Learning**.

---

## 🚀 Overview

- Built with **Google Gemini Pro API** to analyze resumes and extract insights.  
- Implements **PyPDF2** for reading and parsing PDF resumes.  
- Uses **prompt engineering** to compare job descriptions (JD) and resumes for keyword matching.  
- Outputs a structured summary containing:
  - **JD Match Percentage**
  - **Missing Keywords**
  - **Profile Summary**

---

## 🧠 Core Features

- **Resume Analysis:** Extracts text from uploaded PDFs using `PyPDF2`.  
- **LLM-Powered Evaluation:** Uses **Gemini Pro** to semantically compare job description and resume content.  
- **ATS Simulation:** Calculates JD match score and identifies missing keywords.  
- **Interactive Web Interface:** Developed using **Streamlit** for an intuitive and user-friendly experience.  

---

## 🧩 Project Structure
```bash
Smart-ATS/
│
├── app.py # Main Streamlit application
├── .env # Stores your Google API key (not uploaded to GitHub)
├── requirements.txt # Python dependencies
├── README.md # Project documentation
└── sample_resume.pdf # Example resume for testing (optional)
```

---

## ⚙️ How It Works

1. The user uploads a **PDF resume**.  
2. A **job description (JD)** is entered into the text area.  
3. The model extracts resume text using **PyPDF2**.  
4. The prompt template passes both resume and JD to **Google Gemini Pro**.  
5. The model returns a structured JSON-like output:
   ```json
   {
     "JD Match": "85%",
     "MissingKeywords": ["TensorFlow", "AWS", "SQL"],
     "Profile Summary": "Strong foundation in data science and ML with focus on model deployment."
   }


The output is displayed interactively in the Streamlit app.

## 🛠️ Technologies Used

Python

Streamlit – Frontend and UI

Google Gemini Pro API – LLM for resume evaluation

PyPDF2 – Resume text extraction

dotenv – Secure API key management

## ⚙️ Installation and Setup
## 1️⃣ Clone the Repository
```bash
git clone https://github.com/Ibtesum-Sakib/Smart-ATS-Resume-Evaluator.git
```
## 2️⃣ Navigate to the Project Folder
```bash
cd Smart-ATS-Resume-Evaluator
```
## 3️⃣ Create a Virtual Environment
```bash
python -m venv venv
source venv/bin/activate   # On Mac/Linux
venv\Scripts\activate      # On Windows
```
## 4️⃣ Install Dependencies
```bash
pip install -r requirements.txt
```
## 5️⃣ Add Your Google API Key
```bash 
Create a .env file in the project directory and add:

GOOGLE_API_KEY=your_api_key_here
```
## 6️⃣ Run the Application
```bash
streamlit run app.py
```

Now, open the local URL shown in your terminal to access the app.

## 🧠 Prompt Template Used
```bash
input_prompt = """
Hey Act Like a skilled or very experienced ATS (Application Tracking System)
with a deep understanding of tech fields: software engineering, data science, 
data analysis, machine learning, and big data engineering.

Your task is to evaluate the resume based on the given job description.
You must consider the job market is very competitive and you should provide 
the best possible feedback for resume improvement.

Assign a percentage match based on the JD and identify missing keywords with high accuracy.

resume:{text}
description:{jd}

I want the response in one single string having the structure:
{"JD Match":"%","MissingKeywords":[],"Profile Summary":""}
"""
```
----
## 📦 Example Output

| **Metric** | **Result** |
|-------------|------------|
| **JD Match** | 87% |
| **Missing Keywords** | Python, AWS, TensorFlow |
| **Profile Summary** | Strong technical profile with good alignment to ML roles. |


## 🧑‍💻 Author

**Mohammad Ibtesum Sakib**  
📍 Bochum, Germany  
📧 ibtesum38@gmail.com  
🔗 [LinkedIn](https://www.linkedin.com/in/ibtesum) | [GitHub](https://github.com/Ibtesum-Sakib)

---


## 🏷️ GitHub Topics

#GoogleGemini #LLM #Streamlit #ATS #ResumeScanner #DataScience #Python #JobMatching
