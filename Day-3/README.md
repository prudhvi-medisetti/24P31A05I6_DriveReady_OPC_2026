# Sweet Crumbs – Agentic AI Customer Support Assistant (Day 3)

## Project Overview

Sweet Crumbs is an AI-powered customer support assistant designed for a home-based bakery using Python, LangChain and Google Gemini API.

Day 3 focuses on rebuilding the assistant with LangChain, maintaining conversation memory, testing responses automatically and introducing agent creation.

## Features

- AI-powered bakery customer support
- Product catalogue and price information
- Business-specific system prompts
- LangChain prompt templates and output parsing
- Conversation memory
- English and Telugu response instructions
- Automatic Gemini Flash model selection
- Alternative model fallback for temporary API failures
- CSV-based response testing and pass-rate calculation
- Basic LangChain agent creation
- Secure API key management

## Technologies Used

- Python
- Google Colab
- LangChain
- Google Gemini API
- Gemini Flash models
- CSV

## Business Rules

- Plum cake: Rs 500.
- Chocolate cake: Rs 650.
- Cupcake: Rs 80 each.
- Orders require 24 hours' notice.
- All cakes have eggless versions.
- Never promise a delivery time or place.
- Refer unknown information to the owner.
- Calculate order totals carefully.
- Respond politely in English or Telugu in under 50 words.

## Installation and Setup

1. Open `Day3_Gemini_Corrected.ipynb` in [Google Colab](https://colab.research.google.com/).
2. Run the library installation cell:

   ```python
   %pip install -q langchain "langchain-google-genai<4.5" "google-genai>=2.12.1,<3" "google-auth==2.49.0"
   ```

3. Generate an API key at [Google AI Studio](https://aistudio.google.com/apikey).
4. Open Google Colab Secrets.
5. Add the API key with the name `GEMINI_API_KEY`.
6. Enable notebook access.
7. Run all cells sequentially.

## Project Workflow

```text
Customer Query
      ↓
System Prompt + Conversation History
      ↓
LangChain ChatPromptTemplate
      ↓
Google Gemini API (available Flash model)
      ↓
StrOutputParser
      ↓
AI-Generated Customer Response
      ↓
Conversation History Update
```

## Conversation Memory and History

The assistant uses `MessagesPlaceholder` and a Python history list to remember earlier customer messages and responses during the session.

For example, after a customer introduces themselves as Ravi, the assistant can answer a follow-up question about their name. History is stored in memory and is not saved permanently.

## Automated Testing

The notebook creates a `tests.csv` file containing five test questions and expected response keywords.

| Test Question | Expected Keyword |
| --- | --- |
| How much is a plum cake? | 500 |
| Do you make eggless cakes? | eggless |
| Can I get a cake today evening? | 24 hours |
| Do you deliver to Kakinada? | check with the owner |
| What is the price of 6 cupcakes? | 480 |

The `run_tests()` function reports PASS or FAIL for each question and calculates the overall pass rate. Keyword matching is a basic check, not a complete evaluation of answer correctness.

## Agent Creation

The notebook introduces LangChain's `create_agent()` with the Gemini model and bakery system prompt. The agent is initialized with an empty tools list. Tool-based actions and real order processing are not implemented in Day 3.

## AI Safety and Error Handling

The system prompt instructs the assistant to follow bakery rules and avoid making unconfirmed delivery promises. The notebook selects a responding Gemini Flash model and attempts alternatives for temporary API errors. If all models fail, it reports an error.

API keys are retrieved from Colab Secrets or entered securely. Live execution depends on valid API access, compatible packages, quota and model availability. Dedicated prompt injection filtering is not implemented.

## Learning Outcomes

- Understanding chatbots and agents
- Understanding the four components of an agent
- Working with LangChain and Gemini API
- Creating prompt templates and chains
- Implementing conversation memory
- Parsing model responses
- Creating CSV-based test cases
- Calculating test pass rates
- Understanding basic agent creation and API fallback

## Future Enhancements

- Add tools for price lookup and business hours
- Add order logging and tracking
- Integrate a live product catalogue
- Add database integration and persistent memory
- Integrate the assistant with a business website
- Improve response testing and prompt injection protection

## Project Information

Project Name: Sweet Crumbs Home Bakery

Category: Agentic AI – Day 3

Domain: Artificial Intelligence and Home Business

Platform: Google Colab

Notebook: `Day3_Gemini_Corrected.ipynb`
