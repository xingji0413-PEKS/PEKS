# PEKS Public Architecture

## Conceptual Architecture of Knowledge-Driven Medical Device Development

PEKS explores a knowledge-driven approach to medical device development, risk management, traceability, and regulatory documentation.

The public architecture describes the conceptual technical layers without exposing proprietary implementation details.

---

## 1. Architecture Overview

The PEKS public architecture can be represented as:

```text
┌─────────────────────────────────────────────┐
│       Medical Device R&D Knowledge          │
│                                             │
│ Product · Design · Risk · Control           │
│ Verification · Evidence · Context          │
└──────────────────────┬──────────────────────┘
                       │
                       ▼
┌─────────────────────────────────────────────┐
│             Knowledge Structuring           │
│                                             │
│ Concepts · Entities · Attributes · Context  │
└──────────────────────┬──────────────────────┘
                       │
                       ▼
┌─────────────────────────────────────────────┐
│        Relationship & Traceability          │
│                                             │
│ Risk → Control → Verification → Evidence    │
│ Design → Risk → Verification → Documentation│
└──────────────────────┬──────────────────────┘
                       │
                       ▼
┌─────────────────────────────────────────────┐
│          Knowledge-driven Processing        │
│                                             │
│ Analysis · Reuse · Consistency              │
│ Traceability · Change Impact                │
└──────────────────────┬──────────────────────┘
                       │
                       ▼
┌─────────────────────────────────────────────┐
│          Regulatory Documentation           │
│                                             │
│ Structured Outputs · Reports · Records      │
└─────────────────────────────────────────────┘
```

This is a conceptual public architecture.

It is not a representation of the PEKS production software architecture.

---

## 2. Layer 1 — Medical Device R&D Knowledge

The foundation is the underlying knowledge generated throughout medical device development.

Examples include:

- Product information
- Design information
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

These elements may originate from different development activities and information sources.

The key idea is to treat them as connected development knowledge rather than only as isolated document content.

---

## 3. Layer 2 — Knowledge Structuring

Development information needs to be represented in a structured form before relationships can be consistently maintained.

Conceptually:

```text
Unstructured / Distributed Information
                ↓
        Knowledge Structuring
                ↓
Structured Development Elements
```

The structured representation may contain:

- Entities
- Attributes
- Context
- Terminology
- Status
- Source
- Version
- Applicability

The public model intentionally remains at a conceptual level.

It does not expose the PEKS production data model or schema.

---

## 4. Layer 3 — Relationship & Traceability

The third layer represents relationships between development elements.

A simplified example is:

```text
Risk
  ↓
Risk Control
  ↓
Verification
  ↓
Evidence
```

Another relationship chain may connect product and design information to risk:

```text
Product
  ↓
Design
  ↓
Risk
  ↓
Risk Control
  ↓
Verification
```

The purpose is to preserve development context and traceability across related information.

Relationships shown in this public architecture are conceptual examples.

They do not represent the complete PEKS production ontology or internal relationship definitions.

---

## 5. Layer 4 — Knowledge-Driven Processing

Once development knowledge and relationships are structured, they can provide a foundation for knowledge-driven processing.

Conceptually:

```text
Structured Knowledge
        ↓
Relationships
        ↓
Evidence
        ↓
Traceability
        ↓
Knowledge-driven Processing
```

Potential areas of support include:

- Knowledge reuse
- Consistency analysis
- Traceability analysis
- Change impact analysis
- Evidence linking
- Documentation support

These capabilities are presented conceptually.

The public architecture does not disclose PEKS internal algorithms, reasoning rules, or production processing mechanisms.

---

## 6. Layer 5 — Regulatory Documentation

Regulatory and engineering documents can be treated as representations of underlying development knowledge.

Conceptually:

```text
Structured Knowledge
        ↓
Relationships
        ↓
Traceability
        ↓
Document-specific Representation
        ↓
Regulatory Documentation
```

The objective is to support the creation and maintenance of traceable regulatory documentation.

PEKS does not treat document generation itself as the complete automation problem.

The underlying development knowledge, relationships, evidence, and engineering context remain important.

Regulatory suitability and compliance require appropriate professional review and applicable regulatory assessment.

---

## 7. Cross-Layer Traceability

The architecture can also be viewed as a traceability flow:

```text
Development Knowledge
        ↓
Structured Representation
        ↓
Relationships
        ↓
Traceability
        ↓
Evidence
        ↓
Documentation
```

This provides a conceptual bridge between engineering activities and the documents produced from them.

Instead of asking only:

> Which document contains this information?

a knowledge-driven approach can also ask:

> What development knowledge does this information represent, and what other elements is it connected to?

---

## 8. Lifecycle Perspective

Medical device development is a lifecycle process.

The public architecture can therefore be considered across stages such as:

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

Knowledge and relationships may need to remain useful as the product evolves.

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

The actual lifecycle implementation depends on the organization's development and quality processes.

---

## 9. From Documents to Connected Knowledge

A traditional document-centric representation may look like:

```text
Risk Management File
Verification Report
Design Documentation
Test Record
Technical Documentation
```

A knowledge-oriented representation can additionally describe:

```text
Product
   │
   ├── Design
   │
   ├── Requirement
   │
   ├── Risk
   │     │
   │     └── Risk Control
   │              │
   │              └── Verification
   │                       │
   │                       └── Evidence
   │
   └── Documentation
```

The distinction is not that documents become unnecessary.

Rather, documents can be treated as representations of connected development knowledge.

---

## 10. Architecture Principle

The central architectural principle can be summarized as:

```text
Documents
    ↓
are representations of
    ↓
Development Knowledge
    ↓
connected through
    ↓
Relationships
    ↓
supported by
    ↓
Evidence
```

This creates a foundation for traceable and reusable development information.

---

## 11. What the Public Architecture Exposes

This public architecture intentionally exposes only conceptual layers:

- Development knowledge
- Knowledge structuring
- Relationships
- Traceability
- Knowledge-driven processing
- Documentation support

These concepts are sufficient to explain the technical direction of PEKS without exposing the underlying implementation.

---

## 12. What the Public Architecture Does Not Expose

The public architecture does not disclose:

- Production source code
- Complete PEKS ontology
- Production entity definitions
- Production relationship definitions
- Internal database schemas
- Proprietary data models
- Proprietary risk libraries
- Proprietary control libraries
- Production evidence databases
- Internal reasoning rules
- Internal algorithms
- Customer or project data
- Deployment architecture
- Infrastructure configuration

The public architecture should therefore be understood as a conceptual technical representation.

It is not a reverse-engineering specification.

---

## 13. Relationship to the Knowledge Model

The architecture provides the higher-level structure for the public Knowledge Model.

The relationship is:

```text
PEKS Public Architecture
          ↓
PEKS Knowledge Model
          ↓
Risk Traceability Example
```

The architecture describes the layers.

The Knowledge Model describes the concepts and relationships within those layers.

The Risk Traceability Example demonstrates those concepts using synthetic data.

See:

`docs/02-knowledge-model.md`

for the corresponding public Knowledge Model.

---

## 14. Relationship to the Public Example

The public risk traceability example provides a concrete illustration of the architecture.

```text
Architecture
     ↓
Knowledge Model
     ↓
Synthetic Risk Example
     ↓
Traceability Representation
```

The example is intentionally small so that the underlying concept can be understood without exposing production implementation details.

See:

`examples/risk-traceability/`

for the example.

---

## 15. Public Disclosure Boundary

This document is intentionally limited to conceptual architecture.

It does not disclose the PEKS production implementation.

The public technical layer follows the principle:

> **Show the model, not the machinery.**

The architecture is designed to communicate the technical direction, not to provide enough information to reconstruct the PEKS internal system.

---

## Disclaimer

This document describes a conceptual technical architecture for exploring knowledge-driven medical device development, risk traceability, and regulatory documentation.

It is not regulatory advice, a compliance determination, or a substitute for qualified medical device engineering, quality, or regulatory professionals.

The architecture is simplified and does not represent the complete PEKS production architecture, implementation, ontology, data model, software design, or deployment environment.