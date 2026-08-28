# PEKS Knowledge Model

## Structuring Medical Device Development Knowledge

PEKS explores how medical device development information can be represented as structured and connected knowledge.

The objective is not simply to store more information.

The objective is to preserve the meaning, context, relationships, and traceability between development elements.

---

## 1. From Documents to Knowledge

Medical device development produces many types of information:

- Product and design information
- Requirements
- Hazards
- Hazardous situations
- Harms
- Risks
- Risk controls
- Verification activities
- Validation activities
- Evidence
- Regulatory context

In a document-centric workflow, these elements may appear across multiple documents, spreadsheets, records, and systems.

A knowledge-oriented approach asks a different question:

> What are the underlying development elements, and how are they related?

---

## 2. A Simplified Knowledge Model

A simplified representation is:

```text
Product
   │
   ├── has Hazard
   │       │
   │       └── creates Hazardous Situation
   │                    │
   │                    └── may cause Harm
   │
   ├── has Risk
   │
   └── has Risk Control
             │
             ▼
        Verification
             │
             ▼
          Evidence