# 24P31A05I6_DriveReady_OPC_2026

#  Sweet Crumbs – Agentic AI Customer Support Assistant

## Project Overview
Sweet Crumbs is an AI-powered customer support assistant
designed for a home-based bakery using Python, LangChain
and Groq API.

The assistant provides intelligent and polite responses
to customer queries while following predefined business
rules and safety guidelines.

## Features

- AI-powered customer support
- Natural language processing
- Business-specific prompt engineering
- Order-related enquiry handling
- Eggless cake availability information
- Prompt injection detection demonstration
- Secure API key management
- Short and professional responses

## Technologies Used

- Python
- Google Colab
- LangChain
- Groq API
- GPT-OSS 120B
- Llama Prompt Guard 2 22M

## Business Rules

- All cakes are freshly baked to order.
- Orders require at least 24 hours' notice.
- All cakes have eggless versions.
- Never promise delivery times.
- Provide polite and accurate responses.
- Keep responses under 60 words.

## Installation and Setup

1. Open the notebook in Google Colab.

2. Install the required library:

   pip install langchain_groq

3. Generate an API key from:
   https://console.groq.com/keys

4. Open Google Colab Secrets.

5. Add the API key with the name GROQ_API_KEY.

6. Enable notebook access.

7. Run all cells sequentially.

##  Project Workflow

Customer Query
      ↓
System Prompt
      ↓
LangChain + Groq API
      ↓
GPT-OSS 120B Model
      ↓
AI-Generated Customer Response

##  AI Safety

The project separately demonstrates prompt injection
detection using Llama Prompt Guard.

Model: meta-llama/llama-prompt-guard-2-22m

This safety demonstration is not yet integrated into
the main customer support pipeline.

##  Learning Outcomes

- Understanding Agentic AI fundamentals
- Connecting LLMs using Groq API
- Implementing system prompts
- Understanding prompt engineering
- Secure API key management
- Exploring AI safety and prompt injection

##  Future Enhancements

- Conversation memory
- Online cake ordering
- Order tracking system
- Database integration
- Website chatbot integration
- Integrated prompt injection filtering
- Multilingual customer support

## Project Information

Project Name: Sweet Crumbs Home Bakery

Category: Agentic AI – Day 1

Domain: Artificial Intelligence and Home Business

Platform: Google Colab

---

⭐ AI-powered support for smarter small businesses.
