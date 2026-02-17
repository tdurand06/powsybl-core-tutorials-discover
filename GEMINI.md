# PowSyBl Core Tutorials

This project contains various tutorials for [PowSyBl](https://www.powsybl.org/), an open-source framework for power system simulation and grid modeling.

## Project Structure

- `cgmes/`: Tutorials for CGMES (Common Grid Model Exchange Standard).
- `count-network-lines/`: Example for counting network lines.
- `csv-exporter/` / `csv-importer/`: CSV data exchange examples.
- `docs/`: Documentation for the tutorials.
- `downscaling/`: Downscaling tutorial.
- `groovy-modifications/`: Network modifications using Groovy.
- `loadflow/`: Load flow calculation tutorial.
- `merging/`: Network merging tutorial.
- `sensitivity/`: Sensitivity analysis tutorial.
- `sld-custom-node/`: Single Line Diagram custom node tutorial.
- `topology/`: Topology management tutorial.

## Getting Started

Most modules are Maven projects. You can build the entire project from the root:

```bash
mvn clean install
```
