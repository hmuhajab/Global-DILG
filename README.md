# Populating Saudi Arabia Data

This repository contains a Jupyter notebook and related files for processing geographic data related to Saudi Arabia. The goal is to create and populate a knowledge graph that integrates geographic information using RDF, focusing on populated places within Saudi Arabia.

## Repository Contents

- **`populating_SaudiArabia_Data.ipynb`**: The main Jupyter notebook that processes JSON files containing geographic data, generates RDF triples, and updates relationships within the RDF graph.
- **`Global_DLIGS.rdf`**: An RDF ontology file used as a base for loading and populating new geographic data.
- **`Data.zip`**: Contains the raw JSON files and other supporting data required for processing.
- **`Saudi_KG.zip`**: Contains the populated knowledge graph.

## Overview of the Jupyter Notebook

### 1. Install Necessary Libraries
The notebook begins by installing the `rdflib` library, which is used for handling RDF data in Python.

### 2. Loading and Parsing Ontology
The existing ontology RDF file is loaded into a graph structure. This file serves as the foundation for adding new geographic data.

### 3. Processing JSON Data
The notebook defines functions to process GADM and OSM JSON files. For each geographic entity, RDF triples are created, including information such as GADM ID, type, latitude, longitude, and spatial relationships (e.g., containment and neighboring relationships).

### 4. Updating Relationships
After populating the RDF graph, specific relationships like the `ehInside` (inside) property are corrected and updated to reflect accurate spatial containment within the populated places.

### 5. Saving and Verifying
The RDF graph is serialized and saved to a new RDF file. The notebook also includes verification steps to ensure that the relationships have been correctly updated.

## Running the Notebook

To run this notebook, you need to have Python installed along with the `rdflib` library. You can install the required library using:

```bash
pip install rdflib
