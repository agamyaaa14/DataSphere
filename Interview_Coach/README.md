# Interview Coach

![Banner](interview.png)

An AI-powered mock interview app built as an IBM SkillsBuild guided project. In the cloud environment, watsonx.ai credentials and runtime are pre-provisioned. To run locally, you can clone this repo and adapt the credential code with your own API keys.

## How It Works
- Interview flow: A Gradio UI orchestrates a voice-first mock interview. You upload a PDF resume, paste the job description, pick the number of questions, and click Start.
- Voice I/O: Questions are converted to audio with gTTS; your recorded answers are transcribed using faster-whisper.
- State management: Global state tracks `chat_histories`, `interview_step`, `resume_summary`, and `job_summary` to adapt the experience.
- LLM backbone: IBM watsonx.ai foundation models generate summaries, questions, and evaluations.

## Agents (from `myapp.py`)
- Resume_Analyst(resume): Produces a multi-paragraph report summarizing candidate details, key skills, and experience based on the extracted PDF text.
- Job_Description_Expert(job_description): Summarizes the job description, highlighting required skills and preferred experience.
- Interview_Question_Action(chat_histories, resume_summary, job_summary): Chooses the next questioning strategy — either a new topic from the resume or deeper follow-ups — informed by prior answers and summaries.
- Interviewer(resume_summary, job_summary, action, last): Generates the next interview question based on the chosen action; when `last=True`, it wraps up with a concise closing.
- Evaluator(chat_histories, job_summary): Provides an ongoing assessment of candidate fit and performance grounded in the answer history and job summary.
- Pipelines: `text_to_speech_file()` handles question audio generation; `transcribe_audio_faster_whisper()` converts recorded answers to text; `extract_text_from_pdf()` reads resume content.

## IBM SkillsBuild Context
- Guided environment: This project is designed to run within IBM SkillsBuild/Cognitive Class, where credentials and runtime are provided.
- Local runs: To try locally, update credential handling in `myapp.py`:

```python
from ibm_watsonx_ai import Credentials

credentials = Credentials(
	url="https://us-south.ml.cloud.ibm.com",
	# api_key="YOUR_WATSONX_API_KEY",
)
project_id = "YOUR_PROJECT_ID"
```

Replace placeholders with your watsonx.ai API key and project ID, or configure via environment variables and load them in code.

## Setup
```powershell
# From the workspace root
cd "c:\Users\Dell\Desktop\Datasphere\Interview_Coach"

# Create and activate a virtual environment
python -m venv .venv
.\.venv\Scripts\Activate

# Install dependencies
pip install -r requirements.txt
```

## Run the App
```powershell
python myapp.py
```
The app launches locally and also creates a shareable link (Gradio `share=True`).

## Usage
- Upload your PDF resume.
- Paste the job description (use the included sample JD for quick testing).
- Select the number of questions, then click Start.
- Listen to the interviewer’s audio and record your answer.
- Review ongoing feedback and final evaluation in the Performance panel.

## Security & Git Hygiene
- Do not commit certificates: If `gradio/certificate.pem` exists, exclude it from Git. This README is accompanied by a `.gitignore` entry to prevent committing that file.
- Keep API keys secret: Use environment variables or secure vaults; avoid hardcoding secrets in source.

## Troubleshooting
- Credentials: If the LLM doesn’t respond, verify your watsonx.ai credentials and `project_id`.
- Audio: Allow microphone permissions in the browser; ensure system audio devices work.
- Installation: If installs fail, try `python -m pip install --upgrade pip setuptools wheel` and re-run.
