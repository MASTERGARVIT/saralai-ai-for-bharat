# SaralAI – System Design Specification

## 1. System Overview

SaralAI is a serverless, AI-powered conversational system designed to provide personalized and vernacular access to government schemes and public opportunities.

The system follows a modular, scalable architecture built on AWS services.

---

## 2. High-Level Architecture Components

### Frontend
- Web or mobile interface
- Supports text and voice input
- Language selection and display

### Backend Services
- API Gateway: Request routing
- AWS Lambda: Business logic and eligibility processing

### AI & Language Services
- Amazon Bedrock: Conversational reasoning and response generation
- Amazon Translate: Multilingual support
- Amazon Transcribe: Voice-to-text conversion

### Data Layer
- Amazon S3: Storage of scheme documents
- Amazon OpenSearch: Semantic search using RAG

---

## 3. Data Flow

1. User submits a query via text or voice
2. Voice input is converted to text using Transcribe
3. Language is detected and translated if required
4. Intent and context are extracted
5. Relevant scheme data is retrieved from OpenSearch
6. Bedrock performs reasoning and response generation
7. Final response is translated and returned to the user

---

## 4. AI Design (RAG Pattern)

- Government documents stored in S3
- Indexed into OpenSearch with embeddings
- Retrieval-Augmented Generation ensures:
  - Trusted source grounding
  - Reduced hallucination
  - Explainable outputs

---

## 5. Architecture Diagram (Textual Representation)

