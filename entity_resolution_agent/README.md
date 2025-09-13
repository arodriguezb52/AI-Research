# Entity Resolution Agent

This project implements a sophisticated entity resolution system using machine learning and graph databases.

## Overview

The entity resolution agent uses a multi-agent approach to identify and match entities across different datasets. The system combines traditional machine learning techniques with modern LLM capabilities through LangGraph.

## Key Features

- **Multi-Agent Pipeline**: Combines categorical and probabilistic agents for robust entity matching
- **Neo4j Integration**: Uses graph database for efficient similarity search and context retrieval
- **Human-in-the-Loop**: Interactive labeling system for uncertain cases
- **Stress Testing**: Comprehensive evaluation pipeline for performance assessment

## Files

- `entity_resolution_pipeline.ipynb` - Complete entity resolution pipeline with multi-agent LangGraph system
- `.env.example` - Template for environment variables setup
- PowerPoint presentation detailing findings and explanations of the tech stack used
- Data files: `Abt.csv`, `Buy.csv`, `abt_buy_perfectMapping.csv` (download separately from: https://dbs.uni-leipzig.de/research/projects/benchmark-datasets-for-entity-resolution)

## Setup

1. Install required dependencies:
   ```bash
   pip install pandas numpy langchain-openai langchain-neo4j langgraph neo4j tqdm tenacity
   ```

2. Set up Neo4j database (using Docker):
   ```bash
   docker run -p 7687:7687 -p 7474:7474 --env NEO4J_AUTH=neo4j/your_password neo4j:latest
   ```

3. Configure environment variables in `.env` file

## Usage

Run the main notebook:
```bash
jupyter notebook entity_resolution_pipeline.ipynb
```

The pipeline includes:
1. Data loading and preprocessing
2. Neo4j graph database setup
3. Multi-agent entity resolution
4. Human labeling interface
5. Performance evaluation

## Results

The system achieves high precision and recall on entity matching tasks while providing interpretable results through the multi-agent approach.
