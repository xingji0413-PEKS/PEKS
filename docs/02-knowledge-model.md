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
```

This model illustrates a fundamental principle:

> Development knowledge is not only a collection of entities. The relationships between entities are also knowledge.

The relationships shown above are simplified conceptual examples.

They do not represent the complete PEKS production ontology.

---

## 3. Core Knowledge Elements

### Product

Represents the medical device, device family, component, or relevant product context.

Examples may include:

- Device type
- Product configuration
- Components
- Intended use
- Relevant design characteristics

---

### Hazard

Represents a potential source of harm within the relevant development and risk-management context.

In a structured knowledge model, hazards can be connected to the conditions and development elements through which they may contribute to risk.

---

### Hazardous Situation

Represents the circumstances in which a person, property, or environment may be exposed to one or more hazards.

The relationship between:

```text
Hazard
   ↓
Hazardous Situation
```

provides context for subsequent risk analysis.

---

### Harm

Represents potential injury or damage resulting from a hazardous situation.

A simplified relationship is:

```text
Hazard
   ↓
Hazardous Situation
   ↓
Harm
```

---

### Risk

Risk represents an identified development risk within the context of the risk management process.

In this simplified knowledge model, a risk remains connected to the underlying hazard, hazardous situation, harm, and relevant risk controls.

The purpose of the model is to preserve these relationships rather than treating the risk as an isolated document entry.

Conceptually:

```text
Hazard
   ↓
Hazardous Situation
   ↓
Harm
   ↓
Risk
   ↓
Risk Control
```

The example is intentionally simplified and does not attempt to provide a complete representation of risk management requirements.

---

### Risk Control

Represents a measure intended to reduce or otherwise control an identified risk.

A simplified relationship is:

```text
Risk
   ↓
Risk Control
```

The control should remain traceable to the risk it addresses.

In a real development environment, the control may also be connected to design requirements, implementation information, verification activities, and supporting evidence.

---

### Verification

Represents an activity used to provide objective evidence that specified requirements or controls have been met, as applicable to the development context.

A simplified relationship is:

```text
Risk Control
      ↓
Verification
```

Verification activities may have additional relationships to requirements, test methods, acceptance criteria, results, and records.

---

### Evidence

Represents information or records supporting an engineering conclusion, verification result, or other development claim.

A simplified relationship is:

```text
Verification
      ↓
Evidence
```

Evidence can therefore become part of the traceability chain rather than remaining an isolated document reference.

---

## 4. Relationships Are First-Class Knowledge

A conventional information model may focus primarily on entities:

```text
Product
Risk
Control
Verification
Document
```

A knowledge model additionally represents relationships:

```text
Product
   ↓
has Risk

Risk
   ↓
addressed by
   ↓
Risk Control

Risk Control
   ↓
verified by
   ↓
Verification

Verification
   ↓
supported by
   ↓
Evidence
```

These relationships provide context that cannot always be reliably reconstructed from isolated records or document text alone.

The relationship names shown here are illustrative public concepts.

They are not PEKS production ontology predicates.

---

## 5. Example: Risk Knowledge Chain

Consider a simplified example involving a hypothetical balloon catheter.

```text
Product
  │
  ▼
Balloon Catheter
  │
  ▼
Hazard
Mechanical Failure
  │
  ▼
Hazardous Situation
Component Failure During Intended Use
  │
  ▼
Harm
Potential Patient Injury
  │
  ▼
Risk
Mechanical Failure-related Risk
  │
  ▼
Risk Control
Design Control
  │
  ▼
Verification
Mechanical Performance Testing
  │
  ▼
Evidence
Verification Record
```

This is a synthetic and simplified example.

It is intended only to demonstrate the structure of relationships.

It does not represent a complete product-specific risk analysis.

---

## 6. Knowledge Is More Than a Graph

A knowledge model is not simply a collection of nodes and edges.

Useful development knowledge may also require:

- Attributes
- Context
- Terminology
- Units
- Status
- Source
- Version
- Applicability
- Evidence
- Time or lifecycle context

For example:

```text
Risk Control
   │
   ├── Objective
   ├── Status
   ├── Applicable Product
   ├── Related Risk
   ├── Verification
   └── Supporting Evidence
```

The exact structure required depends on the development process and intended application.

The attributes shown above are conceptual examples and do not represent the PEKS production data model.

---

## 7. Context Matters

The same term may have different meanings depending on its context.

For example:

```text
Product
Risk
Control
Verification
Evidence
```

cannot always be interpreted correctly without knowing:

- Which product
- Which configuration
- Which development phase
- Which requirement
- Which risk
- Which applicable context
- Which supporting evidence

Therefore, structured knowledge should preserve context rather than reducing development information to isolated keywords.

Context is particularly important when development information is reused across different products, configurations, lifecycle stages, or documentation outputs.

---

## 8. Lifecycle Perspective

Medical device development knowledge evolves throughout the product lifecycle.

A simplified lifecycle view is:

```text
Concept
   ↓
Design
   ↓
Risk Management
   ↓
Verification & Validation
   ↓
Production
   ↓
Post-Market Information
   ↓
Change / Improvement
```

Knowledge relationships may need to remain useful as the product evolves.

For example:

```text
Design Change
     ↓
Potential Risk Impact
     ↓
Risk Control Review
     ↓
Verification Review
     ↓
Evidence Review
     ↓
Documentation Update
```

This illustrates why knowledge relationships can be more valuable than maintaining independent document copies.

A real implementation would require appropriate change-control processes and professional review.

---

## 9. Knowledge Reuse

Once development knowledge is structured, appropriate information may potentially be reused across multiple outputs.

Conceptually:

```text
                 ┌── Risk Management
                 │
Structured ──────┼── Verification
Knowledge        │
                 ├── Technical Documentation
                 │
                 └── Regulatory Documentation
```

The same underlying development fact should not need to be independently recreated in every document.

Reuse, however, does not imply that the same information is automatically applicable everywhere.

Applicability, context, version, and professional review remain necessary.

---

## 10. Knowledge and Documentation

PEKS distinguishes between:

### Knowledge Layer

```text
Product
Risk
Control
Verification
Evidence
Relationships
Context
```

and:

### Documentation Layer

```text
Risk Management Documents
Verification Reports
Technical Documentation
Regulatory Records
Other Development Documents
```

The relationship can be represented as:

```text
Development Knowledge
        ↓
Relationships
        ↓
Traceability
        ↓
Document-specific Representation
```

Documents remain important.

The distinction is that documents can be understood as representations of underlying development knowledge rather than the only place where that knowledge exists.

---

## 11. Knowledge Model vs. Ontology

This repository intentionally uses the broader term **Knowledge Model**.

A knowledge model describes:

- What concepts are relevant
- What information they contain
- How they relate
- What context they require
- How they participate in a development process

An ontology may provide a more formal representation of concepts, relationships, constraints, and semantics.

PEKS may use ontology-oriented techniques internally, but this public repository does not disclose the complete PEKS ontology.

The examples presented here should therefore be understood as:

> **Public conceptual models, not the production ontology.**

The public knowledge model is intentionally simplified to communicate the technical direction without exposing proprietary implementation details.

---

## 12. Knowledge Model and Traceability

The knowledge model provides the foundation for traceability.

A simplified chain is:

```text
Product
   ↓
Hazard
   ↓
Hazardous Situation
   ↓
Harm
   ↓
Risk
   ↓
Risk Control
   ↓
Verification
   ↓
Evidence
```

Traceability can then be extended toward documentation:

```text
Evidence
   ↓
Development Conclusion
   ↓
Regulatory Documentation
```

This enables development information to be followed across multiple stages rather than being confined to a single document.

Traceability relationships may differ depending on the development activity and applicable context.

---

## 13. Why This Matters for Automation

Text generation can produce a document from structured prompts or other inputs.

A knowledge-driven approach starts from a different foundation:

```text
Structured Knowledge
        ↓
Relationships
        ↓
Evidence
        ↓
Traceability
        ↓
Document Representation
```

The distinction is important.

Generating text is only one part of the problem.

A more fundamental challenge is maintaining the engineering knowledge, relationships, context, and evidence that give the generated content its meaning.

Knowledge-driven processing may therefore support:

- Consistency
- Knowledge reuse
- Traceability
- Change impact analysis
- Evidence linking
- Documentation support

These capabilities are described conceptually in this public repository.

The actual implementation, algorithms, rules, and production knowledge structures are not disclosed.

---

## 14. Knowledge as a Development Asset

When development knowledge is represented as connected information, it can potentially be treated as a reusable engineering asset.

Conceptually:

```text
Development Activity
        ↓
Structured Knowledge
        ↓
Connected Relationships
        ↓
Traceable Evidence
        ↓
Reusable Development Asset
```

This perspective shifts the focus from repeatedly producing documents toward maintaining the underlying development knowledge that documents represent.

The objective is not to eliminate documents.

The objective is to make the knowledge behind those documents more structured, connected, and reusable.

---

## 15. Public Disclosure Boundary

The examples in this document intentionally remain at the conceptual level.

This repository does not expose:

- The complete PEKS ontology
- Production entity definitions
- Production relationship definitions
- Proprietary attributes
- Internal identifiers
- Proprietary risk libraries
- Proprietary control libraries
- Production evidence databases
- Internal database schemas
- Proprietary reasoning rules
- Customer or project data
- Production source code

Public examples may be expanded using synthetic or simplified data.

The structures shown in this document are conceptual examples and should not be interpreted as the PEKS production ontology, data model, database schema, or implementation.

> **Show the model, not the machinery.**

---

## 16. Relationship to the PEKS Public Architecture

The knowledge model corresponds primarily to the first three layers of the PEKS Public Architecture:

```text
Medical Device R&D Knowledge
            ↓
Knowledge Structuring
            ↓
Relationship & Traceability
```

These layers provide the foundation for:

```text
Knowledge-driven Processing
            ↓
Regulatory Documentation
```

See:

`docs/01-public-architecture.md`

for the broader conceptual architecture.

---

## Disclaimer

This document describes a conceptual knowledge model for exploring medical device development knowledge and traceability.

It is not regulatory advice, a compliance determination, or a substitute for qualified medical device engineering, quality, or regulatory professionals.

The examples are simplified and are not intended to represent a complete risk analysis, verification strategy, regulatory submission, production ontology, or production data model.