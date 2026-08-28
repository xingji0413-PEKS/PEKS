# Risk Traceability Example

## Synthetic Medical Device Example

This example demonstrates how a simplified medical device risk can be represented as connected development knowledge.

The example uses a hypothetical balloon catheter and synthetic data.

It is intentionally simplified and does not represent a complete medical device risk analysis.

---

## 1. Objective

The purpose of this example is to demonstrate the relationship between:

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

The example focuses on the relationships between these elements rather than document formatting.

⸻

2. Product

Hypothetical Device

Balloon Catheter

The device is used only as a generic example for demonstrating knowledge relationships.

No real product, customer, or project data is included.

⸻

3. Risk Scenario

A simplified risk scenario is represented as:

Mechanical Failure
        ↓
Component Failure During Intended Use
        ↓
Potential Patient Injury

This scenario is intentionally generic and simplified.

⸻

4. Knowledge Chain

The corresponding development knowledge can be represented as:

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

This chain is intentionally simplified for public demonstration.

⸻

5. Structured Representation

The simplified risk information is represented in:

risk.yaml

The relationships between development elements are represented in:

traceability.yaml

The YAML structures are intentionally simplified public examples and should not be interpreted as the PEKS production schema.

⸻

6. Why Relationships Matter

A document-centric representation might store the following information in separate locations:

Risk Management File
Verification Report
Design Documentation
Test Record
Technical Documentation

A knowledge-oriented representation additionally captures the relationships between them.

For example:

Risk
 ↓
Risk Control
 ↓
Verification
 ↓
Evidence

This makes it possible to ask questions such as:

* Which control addresses this risk?
* How was the control verified?
* What evidence supports the verification?
* Which development conclusions depend on the evidence?

The example demonstrates the principle of connecting development knowledge rather than treating each document as an isolated information container.

⸻

7. Traceability View

The example can be viewed as:

Hazard
   │
   ▼
Hazardous Situation
   │
   ▼
Harm
   │
   ▼
Risk
   │
   ▼
Risk Control
   │
   ▼
Verification
   │
   ▼
Evidence

The chain represents a simplified traceability path.

In a real development environment, additional relationships, attributes, lifecycle states, sources, evidence, and applicable context would be required.

⸻

8. What This Example Demonstrates

This example demonstrates three concepts:

1. Structured Knowledge

Development information can be represented as structured entities.

2. Explicit Relationships

Relationships between entities can be represented explicitly rather than inferred only from document text.

3. Traceability

A development element can be followed through related controls, verification activities, and evidence.

Together, these concepts provide a simple foundation for knowledge-driven development workflows.

⸻

9. What This Example Does Not Demonstrate

This example does not represent:

* A complete risk management process
* A complete ISO 14971 implementation
* A production ontology
* A production risk library
* A production control library
* A regulatory submission
* A complete verification strategy
* A complete evidence database
* PEKS proprietary implementation

The example is intended only to demonstrate the underlying concept of knowledge-based traceability.

⸻

10. Synthetic Data Notice

All device information, identifiers, relationships, and examples in this directory are synthetic or intentionally simplified.

They are provided solely for technical demonstration.

No customer, product, project, or confidential development information is included.

This example demonstrates the conceptual model, not the PEKS production implementation.

⸻

11. Relationship to the PEKS Public Technical Layer

This example builds on the concepts described in:

docs/01-public-architecture.md

and:

docs/02-knowledge-model.md

The relationship between the three layers can be summarized as:

Public Architecture
        ↓
Knowledge Model
        ↓
Risk Traceability Example

The architecture describes the overall direction.

The knowledge model describes the types of development knowledge and their relationships.

This example demonstrates how those concepts can be represented using simplified structured data.

⸻

12. Public Disclosure Boundary

This example intentionally does not expose:

* Production source code
* Complete PEKS ontology
* Production data models
* Internal database schemas
* Proprietary risk libraries
* Proprietary control libraries
* Production evidence databases
* Internal identifiers
* Proprietary reasoning rules
* Customer or project data

The YAML files in this directory are public conceptual examples.

They should not be interpreted as the PEKS production data model, ontology, database schema, or implementation.

Show the conceptual model, not the production machinery.

⸻

Disclaimer

This document describes a conceptual technical example for demonstrating structured medical device development knowledge and traceability.

It is not regulatory advice, a compliance determination, or a substitute for qualified medical device engineering, quality, or regulatory professionals.

The example is simplified and synthetic and is not intended to represent a complete risk analysis, verification strategy, or regulatory submission.


