# Health Analysis

This folder contains a simple blood work analysis pipeline that extracts medical test values from a blood report and generates a diet recommendation using a Google Gemini-backed LLM.

## Contents

- `blood_work_analysis.ipynb`
  - Notebook demonstrating the extraction workflow.
  - Reads the blood report from `blood_work.txt`.
  - Uses `langchain_google_genai.ChatGoogleGenerativeAI` to extract test values and classify them as `HIGH`, `LOW`, or `NORMAL`.
  - Generates a short health summary and an Indian diet recommendation.
- `blood_work.txt`
  - Example blood report text used by the notebook and Streamlit app.
- `Streamlit_app/app.py`
  - Streamlit application version of the notebook workflow.
  - Allows uploading or pasting a blood report and displays both extraction results and diet advice.

## Prerequisites

- Python 3.10+ (or the Python version used by the project environment).
- Install required packages in the project environment, including:
  - `streamlit`
  - `python-dotenv`
  - `langchain_google_genai`

- A `.env` file with the required Google API credentials for `langchain_google_genai`.

## Running the notebook

1. Activate the project virtual environment.
2. Open `Health_analysis/blood_work_analysis.ipynb` in Jupyter or VS Code.
3. Run the notebook cells in order.

## Running the Streamlit app

From the `Health_analysis/Streamlit_app` folder:

```bash
cd "C:\Users\HP\Desktop\Agentic-Project\Health_analysis\Streamlit_app"
streamlit run app.py
```

Then open the URL shown in the terminal.

## Notes

- The Streamlit app loads a default report from `Health_analysis/blood_work.txt` when available.
- If you upload a new report file, the app will use that text instead.
- Make sure your `.env` file is properly configured before running either the notebook or the Streamlit app.
