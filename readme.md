# 📧 Email Classification API with FastAPI and Google Gemini

This project is a FastAPI web application that leverages the Google Gemini API to classify emails based on their content, assigning predefined tags.

## ✨ Features

- **FastAPI Backend:** Built on the modern, fast, and asynchronous FastAPI framework.
- **Google Gemini Integration:** Uses the `gemini-1.5-pro-latest` model for intelligent email analysis.
- **Pydantic Models:** Ensures robust request and response data validation.
- **Environment Configuration:** Securely load API keys using `python-dotenv`.
- **Defined Tags:** Classifies emails into specific categories like "Bug Report", "Feature Request", "Refund Request", etc., plus "Other" and "Spam/Irrelevant".
- **Batch Processing:** Can process multiple emails in a single API request.
- **Clear API Endpoints:** Simple `/` health check and `/classify` POST endpoint.
- **Error Handling:** Includes checks for missing API keys, API errors, and invalid responses.

## 🚀 Getting Started

Follow these steps to set up and run the project locally.

### Prerequisites

- Python 3.7+
- [Google AI Studio](https://aistudio.google.com/) Account to get a Gemini API Key.

### Installation

1.  **Clone the repository** (Assuming this code is in a repo):
    ```bash
    git clone <repository_url>
    cd <repository_directory>
    ```
2.  **Create a virtual environment** (recommended):
    ```bash
    python -m venv .venv
    source .venv/bin/activate # On Windows use `.venv\Scripts\activate`
    ```
3.  **Install dependencies:**
    ```bash
    pip install -r requirements.txt
    ```
    _(Create a `requirements.txt` file with the following content if it doesn't exist)_:
    ```
    fastapi
    uvicorn
    pydantic
    python-dotenv
    google-generativeai
    ```

### Configuration

1.  **Obtain a Google API Key:** Go to [Google AI Studio](https://aistudio.google.com/) and create an API key.
2.  **Create a `.env` file:** In the root directory of the project, create a file named `.env` and add your API key:
    ```dotenv
    GOOGLE_API_KEY=YOUR_API_KEY_HERE
    ```
    _Replace `YOUR_API_KEY_HERE` with the key you obtained._

### Running the Application

Run the application using Uvicorn:

```bash
uvicorn main:app --host 0.0.0.0 --port 8000 --reload
```
