# Clinical RAG Assistant for Electronic Health Records

> **Private Project**
>
> Due to confidentiality agreements, source code, proprietary assets, institution names, and sensitive business information cannot be shared. This document focuses exclusively on the system architecture, engineering decisions, and my technical contributions.

---

## Overview

As the Hospital Information System matured, a new initiative emerged to improve physicians' access to patient information during medical consultations.

I designed and implemented an AI-powered Retrieval-Augmented Generation (RAG) assistant capable of answering natural language questions about a patient's Electronic Health Record (EHR).

The assistant retrieved patient-specific clinical information from the hospital database, built a secure context, and submitted it to a Large Language Model, allowing physicians to interact with medical records through a conversational interface.

---

## Solution Overview

The solution consisted of two independent components:

- Integrated chat interface inside the Hospital Information System
- AI microservice responsible for retrieval, prompt construction, and interaction with the language model

The architecture isolated AI processing from the core EHR while maintaining strict control over patient context.

---

## High-Level Architecture

[IMAGE_PLACEHOLDER_01]
Overall RAG Architecture

[IMAGE_PLACEHOLDER_02]
Example Conversation Flow


Doctor
    │
    ▼
Hospital System
    │
Patient Selected
    │
    ▼
Retrieve Patient Data
    │
    ▼
Build Prompt
    │
    ▼
Gemini / LLM
    │
    ▼
Response
    │
    ▼
Hospital Interface

**Architecture Components**

- Hospital Information System
- Patient Context Retrieval
- RAG Pipeline
- FastAPI Microservice
- Large Language Model
- Conversational Interface

Only information related to the currently selected patient was retrieved before building the prompt, ensuring contextual isolation during every conversation.

---

## My Contributions

### AI Solution Architect

- Designed the overall RAG architecture.
- Defined the patient context retrieval strategy.
- Designed secure prompt construction.
- Integrated the assistant into the existing Hospital Information System.

### AI Engineer

- Developed the backend AI microservice.
- Implemented patient-specific retrieval workflows.
- Connected the assistant to multiple LLM providers.
- Evaluated different model approaches throughout the project.

### Software Engineer

- Developed the integration between the EHR interface and the AI backend.
- Implemented controlled access within the clinical workflow.
- Maintained separation between the monolithic core system and AI services.

---

## Technical Evolution

The project evolved alongside advances in Generative AI.

Initial implementation:

- Fine-tuned BERT model
- Fully On-Premise deployment

Later evolution:

- Google Vertex AI
- Bard API (later Gemini)
- Improved conversational capabilities
- Higher response quality
- Lower infrastructure maintenance

---

## Key Technical Challenges

- Ensuring patient data isolation during every conversation.
- Retrieving only clinically relevant information for each query.
- Integrating AI capabilities into an existing enterprise application.
- Designing a modular architecture without affecting the core hospital system.
- Adapting the solution as Large Language Models rapidly evolved.

---

## Technologies

**Languages**

- Python
- C#
- SQL

**AI**

- Retrieval-Augmented Generation (RAG)
- Large Language Models
- BERT
- Google Vertex AI
- Gemini

**Backend**

- FastAPI

**Infrastructure**

- Docker
- On-Premise Deployment

**Database**

- Microsoft SQL Server

---

## Results

- Successfully integrated conversational AI into a production Hospital Information System.
- Reduced the time required for physicians to access relevant patient information.
- Designed a modular AI architecture independent of the core application.
- Enabled future migration between different LLM providers with minimal architectural changes.

---

## Related Case Studies

- 🏥 Enterprise Hospital Information System
- 🔄 Healthcare Data Integration Platform
- 📊 Clinical Risk Prediction Models
- 💬 Healthcare WhatsApp Notification Platform
