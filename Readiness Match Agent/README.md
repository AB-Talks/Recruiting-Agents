# Readiness Match Agent

## Overview
The Readiness Match Agent computes the alignment between a parsed candidate profile and a parsed job description schema. It acts as an unbiased evaluator to identify skill overlaps and missing requirements.

## Inputs
- **Candidate JSON**: Structured output from the Resume Parser Agent.
- **JD JSON**: Structured output from the JD Parser Agent.

## Outputs
- **Match JSON**:
  - `overall_score` (0-100)
  - `matching_skills`
  - `missing_skills`
  - `experience_gap`
  - `recommendation`

## Dependencies
- `google-generativeai`

## Usage
```python
from match_agent import compute_match

match_results = compute_match(candidate_json, jd_json)
print(match_results)
```
