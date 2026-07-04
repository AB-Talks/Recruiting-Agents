# JD Parser Agent

## Overview
The JD (Job Description) Parser Agent takes raw job description text and transforms it into precise technical requirements, identifying must-have skills, preferred skills, and seniority levels.

## Inputs
- **Raw JD Text**: A string containing the unstructured text of a job description.

## Outputs
- **Structured JSON Schema**:
  - `title`
  - `required_skills`
  - `preferred_skills`
  - `seniority`
  - `experience`
  - `industry`

## Dependencies
- `google-generativeai`

## Usage
```python
from jd_agent import parse_jd

raw_text = """
We are looking for a Senior Python Developer with 5+ years of experience...
"""
result_json = parse_jd(raw_text)
print(result_json)
```
