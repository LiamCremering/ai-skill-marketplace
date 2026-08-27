# Best Practices

Diese Sammlung ergänzt den AI Skill Marketplace um wiederverwendbare Engineering-Prinzipien. Sie ist eine Checkliste für die Phase vor der Implementierung – nicht als schwergewichtiger Prozess, sondern als Hilfe für die Entscheidungen, die später teuer zu ändern wären.

| Prinzip | Ergebnis, das vor der Implementierung vorliegen sollte |
| --- | --- |
| Anforderungen formalisieren | Verständliche Ziele, Akzeptanzkriterien und priorisierte Anforderungen |
| Architektur definieren | Ein nachvollziehbares Systembild mit den wichtigsten Entscheidungen |
| Modularität gestalten | Klare Verantwortlichkeiten und begrenzte Abhängigkeiten |
| Schnittstellen festlegen | Versionierbare Verträge zwischen Teams und Komponenten |
| Betrieb mitdenken | Messbare Ziele für Zuverlässigkeit, Skalierung und Diagnose |

## Design Best Practices

### 1. Formalize Requirement Analysis

**Goal:** Define what the system must do before implementation begins.

**Why:** Clear requirements align stakeholders and prevent scope creep, rework, and inconsistent expectations.

**Before you start, make sure you have:**

- Functional requirements and business rules
- Non-functional requirements, such as latency, availability, privacy, or accessibility
- User stories with clear acceptance criteria
- A shared definition of what is explicitly out of scope

**Useful check:** Can a teammate decide whether a feature is complete without asking the original requester?

### 2. Define Architecture Before Implementation

**Goal:** Establish the system structure before writing code.

**Why:** Early architectural choices prevent costly redesigns and create clear guidance for development teams.

**Before you start, make sure you have:**

- System boundaries and the responsibility of every major component
- The important data flows and integration points
- A record of consequential decisions and their trade-offs
- Explicit assumptions and risks that still need validation

**Useful check:** Could a new team member explain the system's main flow from input to outcome after reading one diagram?

### 3. Design Modular & Maintainable Systems

**Goal:** Build systems that are easy to understand, modify, and extend.

**Why:** Well-structured systems reduce complexity and make future changes less risky.

**Before you start, make sure you have:**

- One clear responsibility per module or service
- High cohesion: related behavior stays together
- Low coupling: implementation details do not leak across boundaries
- Reusable components only where reuse is proven or clearly expected

**Useful check:** Can one module change without requiring coordinated changes throughout the system?

### 4. Define Clear Interfaces & Contracts

**Goal:** Enable independent development and reduce integration failures.

**Why:** Clear interfaces establish predictable communication and minimize ambiguity.

**Before you start, make sure you have:**

- APIs and data contracts with examples for successful and failed requests
- Clear ownership for every interface and data source
- Expectations for validation, authentication, errors, retries, and versioning
- A chosen communication protocol appropriate for the use case

**Useful check:** Could another team implement against the contract without reading your internal code?

### 5. Design for Scalability, Reliability & Observability

**Goal:** Ensure the system performs reliably under real-world conditions.

**Why:** Designing for operational quality avoids outages, performance bottlenecks, and difficult troubleshooting.

**Before you start, make sure you have:**

- Measurable targets for performance, availability, and recovery
- A scaling approach and the expected bottlenecks
- Failure handling for dependencies, retries, timeouts, and degraded modes
- Monitoring, structured logs, and alerts that answer "what failed and why?"

**Useful check:** When the system is slow or unavailable, can the team detect, diagnose, and recover from the problem quickly?

## Development Best Practices

Coming soon.
