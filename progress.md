find# Learning Progress Tracker

This guide provides a recommended path through the PowSyBl tutorials, designed for someone learning both the framework and Java simultaneously.

## 0. Setup & Configuration
Before starting the code tutorials, ensure your environment is ready.

- [x] **IDE Configuration**
    -   **Location:** `docs/intellij.md`
    -   **Goal:** Set up IntelliJ IDEA to work with the project.
    -   **Java Concepts:** Project structure
I did this, but i forked it instead of doing a clone.

## 1. Core Concepts: Topology & Modeling
Start here to understand how power networks are represented in PowSyBl.

- [ ] **Topology Tutorial**
    -   **Location:** `topology/`
    -   **Goal:** Learn how to build a substation, switch between node/breaker and bus/breaker views.
    -   **Java Level:** Beginner.
    -   **Concepts:** Objects, methods, Builders pattern (chaining methods like `.setId(...).add()`), basic control flow.

## 2. Simulation: Load Flow
The "Hello World" of power system simulation.

- [ ] **Load Flow Tutorial**
    -   **Location:** `loadflow/`
    -   **Goal:** Run a load flow calculation on a simple network and after a contingency (line fault).
    -   **Java Level:** Beginner/Intermediate.
    -   **Concepts:** Exception handling, using external libraries (Simulators), configuration files.

## 3. Data Exchange: Simple Formats (CSV)
Learn how to get data in and out using a simple format.

- [ ] **CSV Importer**
    -   **Location:** `csv-importer/`
    -   **Goal:** Read a network from a CSV file.
    -   **Java Level:** Beginner.
    -   **Concepts:** Reading resources/files, static methods (`Main.class.getResourceAsStream`).

- [ ] **CSV Exporter**
    -   **Location:** `csv-exporter/`
    -   **Goal:** Save a network to a CSV file.
    -   **Java Level:** Beginner.
    -   **Concepts:** File paths (`Paths.get`), writing files.

## 4. Advanced Data Exchange: CGMES & Merging
Working with the industry-standard exchange format (CGMES) and handling multiple files.

- [ ] **CGMES & Security Analysis**
    -   **Location:** `cgmes/`
    -   **Goal:** Import CGMES files from different areas (Belgium, Netherlands), merge them, and run security analysis.
    -   **Java Level:** Intermediate.
    -   **Concepts:** Managing resources, complex workflows.

- [ ] **Merging Tutorial**
    -   **Location:** `merging/`
    -   **Goal:** Merge IGM (Individual Grid Model) files, run load flow, and export results.
    -   **Java Level:** Intermediate.
    -   **Concepts:** Data aggregation, updating models.

## 5. Tooling & CLI Extensions
Learn how to create command-line tools using the framework.

- [ ] **Count Network Lines**
    -   **Location:** `count-network-lines/`
    -   **Goal:** Create a simple CLI tool that counts lines in a network file.
    -   **Java Level:** Intermediate.
    -   **Concepts:** Implementing Interfaces (`Tool`), CLI argument parsing, AutoService annotation.

- [ ] **iTools Packaging**
    -   **Location:** `itools-packager/` (and `docs/itools/`)
    -   **Goal:** Learn how to package your custom tools.
    -   **Java Level:** Intermediate (Build system focus).

## 6. Visualization
Generating diagrams from network models.

- [ ] **Custom Single Line Diagram (SLD) Node**
    -   **Location:** `sld-custom-node/`
    -   **Goal:** Generate a Single Line Diagram with a custom symbol (e.g., specific Wind Turbine icon).
    -   **Java Level:** Advanced.
    -   **Concepts:** Inheritance (`extends`), Overriding methods, Inner classes, graphical libraries.

## 7. Advanced Analysis
More complex simulation scenarios.

- [ ] **Sensitivity Analysis**
    -   **Location:** `sensitivity/`
    -   **Goal:** Calculate how sensitive the network is to changes (e.g., phase-shift transformers, injections).
    -   **Java Level:** Intermediate/Advanced.
    -   **Concepts:** Numerical analysis application, JSON output.

- [ ] **Downscaling**
    -   **Location:** `downscaling/`
    -   **Goal:** Map global steady-state hypotheses to a local network.
    -   **Java Level:** Advanced.
    -   **Concepts:** Data mapping algorithms, configuration mapping.

## 8. Scripting (Optional)
Using Groovy for quick network modifications.

- [ ] **Groovy Modifications**
    -   **Location:** `groovy-modifications/`
    -   **Goal:** Script network changes (add/remove loads/lines) using Groovy.
    -   **Java Level:** N/A (Groovy language).
    -   **Concepts:** Scripting dynamic languages on the JVM.

---

**Tip for Java Learners:**
Always look at the `pom.xml` file in each directory. It tells you which libraries (dependencies) are being used. This is crucial for understanding how Java projects are built and linked together.
