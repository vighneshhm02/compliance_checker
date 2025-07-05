# Trustworthy AI Compliance Checker

This project uses the Gemini API to analyze synthetic marketing data for GDPR and CCPA compliance, and also provides A/B testing analysis.

## Project Structure

```
compliance_checker_project/
├── backend/
│   ├── generate_synthetic_data.py
│   ├── compliance_checker.py
│   ├── ab_testing_analyzer.py
│   ├── list_models.py
│   └── run_all.py
├── frontend/
│   ├── public/
│   │   ├── sample_data.json         # Generated data
│   │   ├── compliance_result.txt    # Gemini's output
│   │   └── ab_test_results.json     # A/B testing results
│   └── src/App.js
│   └── ... (other React files)
├── .env                     # Gemini API key
├── requirements.txt
└── README.md
```

## Instructions

### 1. Install Dependencies

```bash
pip install -r requirements.txt
```

### 2. Set Up Environment Variables

Create a `.env` file in the project root and add your Gemini API key:

```
GEMINI_API_KEY=your_api_key_here
```

### 3. Run Backend Processes

Navigate to the `backend` directory and run the `run_all.py` script. This will:
- Generate synthetic data (`sample_data.json`)
- Run GDPR/CCPA compliance checks (`compliance_result.txt`)
- Run A/B testing analysis (`ab_test_results.json`)
- Copy all generated data to `frontend/public/`

```bash
cd backend
python run_all.py
```

### 4. Start Frontend Dashboard

Navigate to the `frontend` directory and start the React development server:

```bash
cd frontend
npm start
```

This will open the dashboard in your browser, where you can switch between Compliance and A/B Testing views.