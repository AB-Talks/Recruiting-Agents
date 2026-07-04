# Resume Parser Agent

## Overview
The Resume Parser Agent is designed to extract structured information from messy PDF resumes. It uses LLMs to normalize varying formats into a clean, predictable JSON schema containing skills, experience, and domain expertise.

## Inputs
- **PDF Resume File**: A raw binary PDF file of the candidate's resume.

## Outputs
- **Structured JSON Profile**: A structured object containing:
  - `candidate_name`
  - `email`
  - `primary_domain`
  - `estimated_experience_years`
  - `skills` (Array of strings)
  - `experience` (Array of objects with titles, companies, durations, and responsibilities)

## Dependencies
- `pdfplumber` (for PDF text extraction)
- `google-generativeai` (for structuring the text)

## Usage
You can run this agent independently by importing its core function:
```python
from resume_agent import parse_resume_pdf

# Pass the PDF file path
result_json = parse_resume_pdf("sample_resume.pdf")
print(result_json)
```
