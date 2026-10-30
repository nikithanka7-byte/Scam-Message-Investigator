# Scam Message Investigator

##  Project Overview

Scam Message Investigator is an AI-powered application that analyzes suspicious SMS messages, emails, job offers, and online messages to identify possible scam indicators.

This project uses the **Gemma 3 1B Large Language Model (LLM)** through Ollama to investigate messages locally. It provides a risk level, warning signs, explanations, and recommended safety actions.

The application is developed using Python and Streamlit.

##  Project Objectives

- Identify possible scam messages using AI.
- Analyze suspicious messages and their warning signs.
- Classify messages based on risk levels.
- Provide explanations for suspicious content.
- Suggest practical safety actions.
- Run the AI model locally using Ollama.

##  Key Features

- Simple and user-friendly Streamlit interface.
- AI-powered scam message investigation.
- Local LLM integration using Gemma 3 1B.
- Three risk levels:
  - Low Concern
  - Medium Concern
  - High Concern
- Displays message type and summary.
- Identifies warning signs with supporting evidence.
- Provides recommended safety actions.
- Shows investigation limitations.
- Handles connection errors and request timeouts.

##  Technologies Used

| Technology | Purpose |
|---|---|
| Python | Programming language |
| Streamlit | Web application interface |
| Ollama | Runs the AI model locally |
| Gemma 3 1B | Message analysis |
| Requests | Sends API requests |
| JSON | Structured AI response |

##  Project Structure

```text
Scam-Message-Investigator/
│
├── app.py
├── requirements.txt
└── README.md
```

## Application preview 
<img width="1348" height="571" alt="image" src="https://github.com/user-attachments/assets/df4e3359-b2a6-4ff1-a2fb-6aba5d0d1992" />
<img width="1345" height="609" alt="image" src="https://github.com/user-attachments/assets/b93223ba-2dcb-4b14-b3a3-39c2e0dad912" />
<img width="1332" height="595" alt="image" src="https://github.com/user-attachments/assets/b61d178c-ea9a-4492-b628-c6ee0384b981" />
<img width="1317" height="589" alt="image" src="https://github.com/user-attachments/assets/43ca757d-5178-44cf-8b33-c76c6bd2c6ab" />



##  Installation and Setup

### Step 1: Install Python

Install Python 3.10 or newer on your computer.

### Step 2: Install Ollama

Download and install Ollama:

https://ollama.com/download

### Step 3: Download the Gemma Model

Open Command Prompt or Terminal and execute:

```bash
ollama pull gemma3:1b
```

### Step 4: Verify the Model

```bash
ollama run gemma3:1b
```

### Step 5: Clone the Repository

```bash
git clone https://github.com/nikithanka7-byte/Scam-Message-Investigator.git
```

### Step 6: Open the Project Folder

```bash
cd Scam-Message-Investigator
```

### Step 7: Install Required Packages

```bash
python -m pip install -r requirements.txt
```

### Step 8: Run the Application

```bash
streamlit run app.py
```

The application will open in your browser.

##  Requirements

The project uses the following Python packages:

```text
streamlit>=1.40,<2.0
requests>=2.31,<3.0
```

##  Project Workflow

1. The user enters a suspicious message in the Streamlit application.
2. The user clicks the Investigate Message button.
3. The application sends the message and system prompt to the Ollama API.
4. Gemma 3 1B analyzes the message.
5. The AI generates a structured JSON response.
6. Python processes the JSON response.
7. Streamlit displays the investigation report.

## Risk Classification

| Risk Level | Description |
|---|---|
| Low Concern | No clear suspicious indicators found |
| Medium Concern | Some suspicious indicators identified |
| High Concern | Multiple serious warning signs identified |

##  Sample Test Messages

**Test 1: Suspicious Bank Message**

Input:
"Your bank account will be blocked today. Click this link and enter your OTP."

Expected Result: High Concern.

**Test 2: Job Offer Scam**

Input:
"Pay ₹999 registration fees to receive your work-from-home appointment letter."

Expected Result: Medium/High Concern.

**Test 3: Normal College Message**

Input:
"Your practical examination is scheduled for Monday at 10 AM. Please bring your record notebook."

Expected Result: Low Concern.

##  Error Handling

The application handles common errors:

- Connection Error: When Ollama is not running.
- Timeout Error: When the AI model takes too long to respond.
- Invalid Response: When the generated JSON cannot be processed.

##  Safety and Limitations

- The application provides an AI-generated assessment, not a guaranteed scam verdict.
- It analyzes message text only.
- It cannot independently verify sender identities or URLs.
- A Low Concern result does not guarantee that a message is safe.
- Users should verify suspicious requests through official channels.
- Never enter real passwords, PINs, or OTPs into test messages.
- Message analysis is sent to the locally running Ollama service.

##  Future Enhancements

- Add image-based scam detection.
- Integrate URL safety checking.
- Add email scam detection.
- Support multiple languages.
- Maintain investigation history.
- Improve AI analysis accuracy.

##  Developed By

**Nikitha R.**



