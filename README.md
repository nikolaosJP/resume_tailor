# Resume Tailor

Resume Tailor is a Python tool that uses LLMs (currently only compatible with Google's Gemini API) to automatically tailor a LaTeX-based resume to a specific job description for free. It helps you customize your resume for different job applications quickly and efficiently.

## Installation

### Prerequisites
- Python 3.8+
- LaTeX distribution (e.g., [TeX Live](https://www.tug.org/texlive/))

### Steps
1. Clone the repo:
   ```bash
   git clone https://github.com/nikolaosJP/resume-tailor.git
   cd resume-tailor
   ```
2. Create and activate a virtual environment:
   ```bash
   python -m venv r_tailor
   source r_tailor/bin/activate 
   ```
3. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```

---

## Usage

1. **Prepare Your Files**:
   - Edit your LaTeX resume: Modify `/resume/maincontent.tex`.
   - Add the job description: Edit `/job_description.txt`.
   - (Optional) Customize LLM instructions: Edit `/instructions.txt`.

2. **Run the Tool**:
   ```bash
   python main.py
   ```

3. **Check Outputs**:
   Generated files in `/output`:
   - `tailored_resume.tex` (Tailored LaTeX resume)
   - `tailored_resume.pdf` (Compiled PDF)
   - `analysis.md` (Summary of changes)

---

## Configuration

1. Get a [Google Gemini API key](https://ai.google.dev/).
2. Set the API Key as an env varaible:
   - Open your terminal and run:
     ```bash
     export GEMINI_API_KEY="your_api_key_here"
     ```
   - To make this permanent, add the line above to your `~/.bashrc` or `~/.zshrc` file:
     ```bash
     echo 'export GEMINI_API_KEY="your_api_key_here"' >> ~/.bashrc  # or ~/.zshrc
     source ~/.bashrc  # Reload the configuration
     ```
---
