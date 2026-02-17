# Requirements: PowSyBl Mastery Certification (Full Tutorial)

## 1. Document Control
| Metadata | Value |
| :--- | :--- |
| **Version** | 1.1.0 |
| **Status** | **APPROVED** |
| **Context** | Full Repository Mastery (Developer Persona) |
| **Last Updated** | Tuesday, February 17, 2026 |

## 2. Executive Summary
**Vision:** Transform from an "intimidated observer" to a "confident PowSyBl developer" by systematically deconstructing the repository into four digestible tiers of complexity.
**Key Drivers:** API Mastery, elimination of technical debt in understanding, and the ability to programmatically manipulate and simulate large-scale power systems.

## 3. Functional Requirements (The "What")

### Tier 1: Foundations (The "Static" Grid)
| ID | Priority | Feature | Success Metric (Definition of Done) |
| :--- | :--- | :--- | :--- |
| **REQ-T1-01** | **MUST** | Topology Mapping | Successfully traverse the IIDM graph and identify the difference between Bus-Breaker and Node-Breaker models. |
| **REQ-T1-02** | **MUST** | Element Discovery | Use the API to programmatically count and filter specific network elements (Lines, Transformers, Generators). |

### Tier 2: Simulations (The "Dynamic" Grid)
| ID | Priority | Feature | Success Metric (Definition of Done) |
| :--- | :--- | :--- | :--- |
| **REQ-T2-01** | **MUST** | Solver Execution | Configure and run a Load Flow solver that reaches convergence on a standard test case. |
| **REQ-T2-02** | **MUST** | Failure Injection | Intentionally modify network parameters (e.g., impossible V-limits) to trigger and interpret a solver crash/non-convergence. |
| **REQ-T2-03** | **SHOULD** | Sensitivity Analysis | Programmatically determine the impact of a single branch outage (N-1) on the rest of the grid. |

### Tier 3: Data Plumbing (The "Real World" Grid)
| ID | Priority | Feature | Success Metric (Definition of Done) |
| :--- | :--- | :--- | :--- |
| **REQ-LF-01** | **MUST** | Solver Configuration | As a Modeler, I want to understand how to select and configure a Load Flow engine (e.g., Newton-Raphson). |
| **REQ-LF-02** | **MUST** | Parameter Mapping | As a Modeler, I want to map physical properties (P, Q, V limits) to the network elements to ensure convergence. |
| **REQ-LF-03** | **MUST** | Convergence Analysis | As a Modeler, I must be able to identify *why* a Load Flow fails (Non-convergence vs. Data error). |
| **REQ-LF-04** | **SHOULD** | Result Interpretation | As a Modeler, I want to extract and report voltage levels and branch loadings after simulation. |
| **REQ-LF-05** | **WON'T** | Manual Optimization | We will focus on the *execution* of the solver, not the *optimization* of the solver's internal algorithms. |

### Tier 4: Automation (The "Expert" Modeler)
| ID | Priority | Feature | Success Metric (Definition of Done) |
| :--- | :--- | :--- | :--- |
| **REQ-T4-01** | **MUST** | Groovy Scripting | Perform mass-modifications of network elements (e.g., "Set all generator targets to 0.95pu") using Groovy scripts. |
| **REQ-T4-02** | **SHOULD** | Tool Packaging | Package a custom modeling workflow into a CLI tool using the `itools` framework. |

## 4. Non-Functional Requirements (Pedagogic Constraints)
*   **Time-to-Map:** Each tutorial module should be understandable within 30 minutes of focused reading.
*   **Atomic Verification:** Every module must have a "Verification Command" (e.g., `mvn exec:java`) that produces a clear, logged output confirming success.
*   **Zero-State Start:** Tutorials must not assume the user has pre-configured databases or complex local environments.

## 5. Data Dictionary
*   **IIDM:** Interim Internal Data Model. The core Java object graph representing the grid.
*   **Node-Breaker:** A high-fidelity representation of a substation including individual switches.
*   **Bus-Breaker:** A simplified representation where switches are abstracted into connectivity nodes.
*   **Slack Bus:** The reference bus in a load flow that compensates for system losses.

## 6. Out of Scope
*   Writing new mathematical solvers from scratch.
*   GUI development or frontend integration.
*   Non-Java/Groovy API implementations (e.g., Python/pypowsybl is deferred).
