# PEKS

## Knowledge-Driven Medical Device Development

PEKS explores a knowledge-driven approach to medical device development, risk traceability, and regulatory documentation.

The central idea is simple:

> Medical device development is not only a collection of documents.  
> It is a body of connected knowledge, relationships, and evidence.

PEKS explores how this knowledge can be structured, connected, traced, and reused across development activities and documentation.

---

## Why PEKS?

Medical device development generates information across many activities:

- Product development
- Design
- Requirements
- Risk management
- Risk controls
- Verification and validation
- Evidence generation
- Regulatory documentation
- Lifecycle changes

In many workflows, this information is distributed across documents, spreadsheets, records, and systems.

As a result, an important engineering relationship may exist across multiple artifacts without being represented as an explicit connection.

For example:

```text
Risk
  ↓
Risk Control
  ↓
Verification
  ↓
Evidence
```

The information may exist.

The challenge is maintaining the relationship.

PEKS explores this problem from a knowledge-engineering perspective.

---

## From Documents to Connected Knowledge

A simplified conceptual flow is:

```text
Development Information
          ↓
Knowledge Structuring
          ↓
Relationships
          ↓
Traceability
          ↓
Evidence
          ↓
Knowledge-driven Processing
          ↓
Documentation
```

The objective is not simply to generate documents faster.

The objective is to better represent and maintain the development knowledge behind those documents.

---

## Public Architecture

The PEKS public technical architecture can be represented as:

```text
┌─────────────────────────────────────────────┐
│       Medical Device R&D Knowledge          │
└──────────────────────┬──────────────────────┘
                       ↓
┌─────────────────────────────────────────────┐
│             Knowledge Structuring           │
└──────────────────────┬──────────────────────┘
                       ↓
┌─────────────────────────────────────────────┐
│        Relationship & Traceability          │
└──────────────────────┬──────────────────────┘
                       ↓
┌─────────────────────────────────────────────┐
│          Knowledge-driven Processing        │
└──────────────────────┬──────────────────────┘
                       ↓
┌─────────────────────────────────────────────┐
│          Regulatory Documentation           │
└─────────────────────────────────────────────┘
```

This is a conceptual public architecture.

It does not represent the PEKS production software architecture.

See:

[`docs/01-public-architecture.md`](docs/01-public-architecture.md)

---

## Knowledge Model

A simplified PEKS knowledge model connects development concepts such as:

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

The important point is not only the individual concepts.

The relationships between them are also part of the knowledge.

See:

[`docs/02-knowledge-model.md`](docs/02-knowledge-model.md)

---

## Risk Traceability Example

This repository includes a small synthetic example demonstrating how a simplified medical device risk can be represented as connected development knowledge.

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

The example uses a hypothetical balloon catheter and synthetic data.

See:

[`examples/risk-traceability/`](examples/risk-traceability/)

The structured example is available in:

[`examples/risk-traceability/traceability.yaml`](examples/risk-traceability/traceability.yaml)

The example is intentionally simplified and does not represent a complete medical device risk analysis.

---

## Architecture Abstraction Levels

PEKS can be described at different levels of abstraction.

At the higher architectural level, PEKS can be understood through two collaborating capabilities:

```text
Knowledge Layer
       ↕
Reasoning Layer
```

The public technical architecture provides a more granular conceptual decomposition:

```text
Development Knowledge
        ↓
Knowledge Structuring
        ↓
Relationship & Traceability
        ↓
Knowledge-driven Processing
        ↓
Documentation
```

These views are complementary rather than competing architectures.

The two-layer view describes the principal architectural capabilities.

The public technical view decomposes the knowledge and processing flow into understandable stages without exposing the production implementation.

---

## What This Repository Demonstrates

The Public Technical Layer focuses on several principles:

### 1. Structured Knowledge

Development information can be represented as structured concepts rather than remaining only inside documents.

### 2. Relationships

The relationships between development elements can be represented explicitly.

### 3. Traceability

Risk, control, verification, and evidence can be connected into traceable chains.

### 4. Knowledge Reuse

Structured knowledge may support reuse across multiple development and documentation activities.

### 5. Documentation as Representation

Documents can be understood as representations of underlying development knowledge rather than the only location where that knowledge exists.

---

## What This Repository Does Not Provide

This repository intentionally does not expose the PEKS production implementation.

It does not contain:

- Production source code
- Complete production ontology
- Production entity definitions
- Production relationship definitions
- Internal database schemas
- Proprietary data models
- Proprietary risk libraries
- Proprietary control libraries
- Production evidence databases
- Internal reasoning rules
- Internal algorithms
- Customer data
- Project data
- Deployment architecture
- Infrastructure configuration

The examples are conceptual and synthetic.

They should not be interpreted as the PEKS production ontology, database schema, software architecture, or implementation.

---

## Public Disclosure Principle

> **Show the model, not the machinery.**

The purpose of this repository is to make the technical direction understandable and discussable without exposing proprietary implementation details.

The public layer therefore focuses on:

```text
Concepts
   ↓
Architecture
   ↓
Knowledge Model
   ↓
Relationships
   ↓
Traceability
   ↓
Synthetic Example
```

rather than production implementation.

---

## Repository Structure

```text
PEKS/
│
├── README.md
│
├── docs/
│   ├── 01-public-architecture.md
│   └── 02-knowledge-model.md
│
└── examples/
    └── risk-traceability/
        ├── README.md
        └── traceability.yaml
```

---

## Intended Audience

This public technical layer may be useful for people interested in:

- Medical device development
- Medical device risk management
- Regulatory documentation
- Knowledge engineering
- Engineering traceability
- Regulatory technology
- Structured development knowledge
- Knowledge-driven software systems

The repository is intended primarily as a technical and conceptual reference.

It is not a complete software distribution.

---

## Relationship to Medical Device Development

PEKS focuses on the information and knowledge relationships that exist throughout medical device development.

A simplified lifecycle perspective is:

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

Knowledge and relationships may need to remain useful as products and their documentation evolve.

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

The actual implementation of these processes depends on the applicable development, quality, and regulatory context.

---

## Current Scope

The current public release focuses on:

```text
Knowledge
+
Relationships
+
Traceability
+
Evidence
+
Documentation
```

Future public releases may expand the conceptual examples where appropriate.

Any future disclosure will continue to respect the separation between public technical concepts and proprietary production implementation.

---

## Version

**Public Technical Layer V1.0**

Release:

`v1.0.0`

This version represents the initial public technical layer of PEKS.

---

## Disclaimer

This repository describes a conceptual approach to knowledge-driven medical device development, risk traceability, and regulatory documentation.

It is not regulatory advice, a compliance determination, or a substitute for qualified medical device engineering, quality, or regulatory professionals.

The examples are synthetic and intentionally simplified.

They do not represent a complete risk analysis, verification strategy, regulatory submission, production ontology, production data model, or production software implementation.

---

## PEKS

**Knowledge-driven development for regulated workflows.**

> **Show the model, not the machinery.**