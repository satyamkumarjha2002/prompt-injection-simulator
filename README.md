# Prompt Injection & Jailbreak Defense Simulator

This simulator tests the effectiveness of various defense mechanisms against prompt injection and jailbreak attempts on GPT-3.5 Turbo.

## Features

- Tests 5 different types of prompt injection attacks
- Implements Safe Mode with pattern detection
- Records and logs all attack attempts
- Saves results to JSON for analysis
- Multiple defense mechanisms

## Setup

1. Install the required dependencies:
```bash
pip install -r requirements.txt
```

2. Set up your OpenAI API key:
   - Create a `.env` file in the project root
   - Add your API key: `OPENAI_API_KEY=your-api-key-here`

## Usage

Run the simulator:
```bash
python prompt_injection_simulator.py
```

The script will:
1. Run all attack tests with Safe Mode ON
2. Run all attack tests with Safe Mode OFF
3. Save results to `attack_results.json`

## Defense Mechanisms

1. **Safe Mode Pattern Detection**: Checks for known injection patterns
2. **System Prompt Hardening**: Uses a robust system prompt
3. **Response Validation**: Validates AI responses
4. **Pattern-based Filtering**: Filters out suspicious patterns
5. **Logging and Monitoring**: Records all attempts for analysis

## Attack Types Tested

1. Basic prompt injection
2. Developer mode injection
3. Game-based injection
4. Test-based injection
5. Developer impersonation

## Results

Results are saved in `attack_results.json` with the following information:
- Timestamp
- Attack description
- Attack prompt
- Safe mode status
- AI response
- Whether the attack was blocked
- Patterns found (if any)