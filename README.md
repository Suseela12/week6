# Experiment 6: Role-Based and Negative Prompting

## Aim
To study how role-based prompting and negative prompting influence the tone, vocabulary, and instruction adherence of LLM responses.

## Problem Statement
Generate responses to the same question, "Explain the importance of exercise," using three prompt variations: baseline, role-based, and role-based with negative constraints.

## Technologies Used
- Python
- Google Gemini AI
- Google Gen AI SDK

## Prompt Variations

### 1. Baseline
Explain the importance of exercise.

### 2. Role-Based
You are a motivational fitness coach. Explain the importance of exercise.

### 3. Role + Negative Prompting
You are a motivational fitness coach. Do not use any medical jargon. Do not mention weight loss. Explain the importance of exercise.

## Algorithm
1. Initialize the Gemini API client.
2. Define all three prompt versions.
3. Send each prompt to the same model using identical parameters.
4. Print and save the generated responses.
5. Compare tone and vocabulary.
6. Check whether the negative constraints were respected.
7. Save the results to a text file.

## Installation

```bash
pip install -r requirements.txt
```

## Configuration
Set the `GEMINI_API_KEY` environment variable before execution. Never upload API keys to GitHub.

## Execution

```bash
python src/main.py
```

## Expected Output
- Three prompts and their generated responses.
- Response word counts.
- Tone and vocabulary comparison.
- A basic check for forbidden terms.
- Results saved in `output/prompt_results.txt`.

## Result
The experiment compares how role instructions and negative constraints influence LLM-generated text.

## Conclusion
Role-based prompting can guide the model toward a specific tone and style. Negative prompting can reduce unwanted content, but instructions are not guaranteed to be followed perfectly. The generated responses should be reviewed to verify constraint adherence.


└── README.md
```
