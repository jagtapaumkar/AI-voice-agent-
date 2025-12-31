# AI Voice & Text Agent for Automated Customer Support

An AI-driven system that automates end-to-end customer support workflows using voice and text interfaces.  
Designed to reduce manual effort, eliminate unnecessary intermediaries, and intelligently escalate only when human intervention is required.

---

## 🚀 Overview

This project implements an AI-powered support agent capable of understanding user queries, retrieving relevant organizational information, and responding naturally through text or voice.

The system supports:
- FAQ resolution
- Service request registration
- Complaint logging
- Human-in-the-loop escalation for sensitive or out-of-scope cases

All interactions are handled through an event-driven automation architecture and have been fully tested end to end.

---

## 🎯 Problem Statement

Traditional customer support systems often suffer from:
- Repetitive manual handling of common queries
- Multiple layers of human intervention
- Delayed response times
- Poor scalability

This project addresses these issues by automating the complete interaction flow while retaining human oversight where required.

---

## 🧩 System Capabilities

- Text and voice-based customer interaction
- Context-aware AI responses using short-term memory
- Tool-driven intent handling (FAQs, services, complaints)
- Secure human approval for critical actions
- Real-time response delivery

---

## 🧠 High-Level Architecture

Telegram Trigger
↓
Input Normalization (Text / Transcription)
↓
AI Agent (LLM + System Prompt)
↓
Context Memory (Last 5 Messages)
↓
Tool Selection Logic
├─ FAQ Lookup
├─ Service Registration
├─ Complaint Logging
└─ Human-in-the-Loop Escalation
↓
Response Generation
↓
Text or Voice Reply (Telegram)


---

## 🔄 Detailed Workflow

### 1. Message Ingestion
- User initiates interaction via Telegram (text or voice).
- A Telegram trigger captures the incoming message instantly.

---

### 2. Voice Handling (Optional)
- If a voice message is received:
  - Speech is transcribed into text.
  - The transcribed content is forwarded to the AI Agent.
  - Final responses can be converted back into speech and returned as a voice note.

---

### 3. AI Agent Processing
- User input is passed to a centralized AI Agent.
- The agent is connected to a Large Language Model (LLM) such as OpenAI or Google Gemini.
- A carefully designed system prompt governs:
  - Scope of responses
  - Allowed actions
  - Safety and escalation rules

---

### 4. Context & Memory
- The agent maintains a short-term memory of the last five user messages.
- This enables:
  - Context-aware conversations
  - Follow-up question handling
  - Reduced repetition

---

### 5. Tool-Based Intent Resolution
Based on user intent, the AI Agent dynamically routes the request to appropriate tools:

- **FAQ Knowledge Base**  
  Structured data stored in Google Sheets for instant retrieval.

- **Service Registration System**  
  Captures and records user service requests.

- **Complaint Management System**  
  Logs complaints with relevant details for further processing.

---

### 6. Human-in-the-Loop Escalation
For sensitive or restricted queries (e.g., payments, policy exceptions):

- A concise summary is sent to a designated human reviewer.
- The reviewer approves or rejects the action.
- Based on the decision:
  - The workflow proceeds automatically, or
  - The user is informed that a human agent will follow up.

This ensures reliability, compliance, and safety.

---

### 7. Response Delivery
- Final responses are sent back to the user via Telegram.
- Text queries receive text responses.
- Voice queries receive voice responses using Text-to-Speech.

---

## ⚙️ What Was Built vs Integrated

### Built
- End-to-end automation workflows
- AI agent orchestration logic
- Tool routing and decision control
- Telegram and web-based integrations
- Voice-to-text and text-to-voice pipelines

### Integrated
- Large Language Models (LLMs)
- Speech-to-Text and Text-to-Speech services
- Google Sheets as structured data sources
- Messaging platform APIs

---

## ⚠️ Limitations

- System accuracy depends on the quality of provided knowledge sources.
- Only short-term conversational memory is implemented.
- Highly ambiguous or complex queries require human review.

---

## 🎥 Demo Video

The demo video demonstrates:
1. Text-based interaction via Telegram
2. Voice input transcription and processing
3. Automated FAQ resolution
4. Service and complaint registration
5. Human-in-the-loop approval workflow
6. Final response delivery

---

## 🛠 Tech Stack

- JavaScript
- Python
- Large Language Models (OpenAI / Gemini)
- Telegram Bot API
- Speech-to-Text & Text-to-Speech services
- Workflow automation platform
- Google Sheets

---

## ✅ Project Status

- Fully implemented
- Tested end to end
- Production-ready workflow logic

---

## 📌 Future Enhancements

- Long-term memory support
- Multilingual interaction
- Analytics dashboard for conversation insights
- Role-based access for human reviewers
