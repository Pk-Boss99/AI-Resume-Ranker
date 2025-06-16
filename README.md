AI-Powered Resume Ranker
This project evaluates the effectiveness of NLP techniques in ranking resumes based on their relevance to a job description. Built with Streamlit, PyPDF2, and custom NLP implementations in Python, the system allows users to upload resume PDFs and input job descriptions to receive a real-time relevance analysis.

Project Objective
To develop a Streamlit web application that efficiently ranks uploaded resume PDFs against a given job description, leveraging fundamental NLP algorithms (TF-IDF and Cosine Similarity) to quantify textual similarity for talent acquisition.

Key Components / Input Processing Flow
Component

Description

Technologies/Algorithms

Job Description Input

User provides the target job description text.

Streamlit st.text_area

Resume PDF Uploads

Users upload multiple resume PDF files for analysis.

Streamlit st.file_uploader

Text Extraction

Extracts raw text content from the uploaded PDF documents.

PyPDF2

Text Preprocessing

Cleans and tokenizes text (lowercase conversion, non-alphanumeric removal).

Python (string methods, regex)

TF-IDF Calculation

Quantifies the importance of terms within documents relative to the corpus.

Custom Python implementation

Vector Representation

Transforms processed texts into numerical vectors based on TF-IDF scores.

NumPy, Custom Python implementation

Cosine Similarity

Measures the textual similarity between job description and resume vectors.

Custom Python implementation

Ranked Results Display

Presents resumes sorted by their calculated relevance score.

Streamlit st.expander, st.write

Tech Stack
Frontend: Streamlit

Backend & ML Core: Python, NumPy

PDF Processing: PyPDF2

NLP Algorithms: TF-IDF, Cosine Similarity

Standard Python Modules: math, collections, io

How To Run the Project
Follow these steps to set up and run the application on your local machine.

# Step 1: Navigate to your project directory (replace with your actual path)
cd D:\Resume_Ranker

# Step 2: Create a Virtual Environment
python -m venv venv

# Step 3: Activate the Virtual Environment
# On Windows (PowerShell):
.\venv\Scripts\Activate.ps1
# On Windows (Command Prompt/CMD):
# venv\Scripts\activate.bat
# On macOS/Linux/Git Bash:
# source venv/bin/activate

# Step 4: Install All Required Python Packages (ensure requirements.txt is correct)
pip install --no-cache-dir -r requirements.txt

# Step 5: Run the Streamlit App
python -m streamlit run resume_ranker_app.py

Project Structure
For this version, the project follows a simplified structure with core logic within a single application file:

resume_ranker/
│
├── resume_ranker_app.py  # Main Streamlit application with all logic
└── requirements.txt      # Python dependencies

Future Improvements
Advanced NLP Integration: Incorporate libraries like SpaCy or Hugging Face Transformers for more sophisticated parsing, named entity recognition, and semantic similarity, potentially leading to more accurate rankings.

Robust Text Extraction: Enhance PDF text extraction to better handle complex layouts, tables, and images.

User Authentication & Data Persistence: Implement a backend (e.g., Firebase Firestore) to allow users to save job descriptions, uploaded resumes, and past ranking results.

Keyword Highlighting: Visually highlight key matching terms or skills within the ranked resumes to provide immediate insights.

Alternative Ranking Models: Explore other machine learning models or ensemble techniques for ranking beyond basic TF-IDF and Cosine Similarity.

Dockerization: Containerize the application using Docker for easier deployment and environment consistency.

License
This project is open-source and licensed under the MIT License.

Author
Pushkar Kumar
AI/ML Research Enthusiast
Email: hacker.boss.pk@gmail.com

Acknowledgments
Streamlit: For providing an excellent framework for building interactive Python web applications.

PyPDF2: For enabling robust PDF text extraction.

NumPy: For providing essential numerical computing capabilities.

The NLP Community: For the foundational concepts of TF-IDF and Cosine Similarity.
