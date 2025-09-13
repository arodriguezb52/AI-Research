# Research Projects

This repository contains various research projects and experiments related to AI agents, entity resolution, and financial analysis.

## Project Overview

This repository is focused on cutting-edge research in artificial intelligence, specifically:
- **Entity Resolution**: Advanced techniques for matching and deduplicating entities across datasets
- **Financial Analysis Agents**: AI-powered agents for financial document analysis and insights
- **LangGraph Experiments**: Exploration of graph-based language models and reasoning

## Projects

### 🔍 Entity Resolution Agent
- **Location**: `entity_resolution_agent/`
- **Description**: Advanced multi-agent entity resolution system using LangGraph and Neo4j
- **Key Features**:
  - Multi-agent LangGraph workflow with categorical and probability-based decision making
  - Neo4j graph database integration for product relationship modeling  
  - OpenAI GPT-4o-mini powered AI agents
  - Human-in-the-loop labeling system for continuous improvement
  - Comprehensive evaluation metrics (precision/recall)
- **Main Files**: 
  - `entity_resolution_pipeline.ipynb` - Complete entity resolution pipeline with multi-agent system
  - `README.md` - Detailed project documentation and setup instructions

## Technology Stack

- **Languages**: Python, Cypher (Neo4j)
- **ML/AI Frameworks**: LangChain, LangGraph, OpenAI GPT models
- **Databases**: Neo4j (graph database)
- **Data Processing**: Pandas, NumPy
- **Visualization**: Jupyter Notebooks
- **Version Control**: Git

## Getting Started

### Prerequisites
- Python 3.8+
- Neo4j database (for entity resolution projects)
- OpenAI API key
- Required Python packages (see individual project requirements)

### Installation

1. Clone this repository:
   ```bash
   git clone https://github.com/arodriguezb52/Research.git
   cd Research
   ```

2. Set up your environment variables:
   ```bash
   cp .env.example .env
   # Edit .env with your API keys and configuration
   ```

3. Install dependencies for specific projects (see individual project folders)

### Usage

Navigate to the specific project folder and run the Jupyter notebooks:

```bash
cd entity_resolution_agent
jupyter notebook stress_test_pipeline.ipynb
```

## Research Methodology

Each project follows rigorous research practices:
- **Reproducible experiments** with fixed random seeds
- **Comprehensive evaluation** with precision, recall, and F1 metrics
- **Human-in-the-loop validation** for quality assurance
- **Stress testing** for robustness validation
- **Version-controlled experimentation** for iterative improvements

## Results and Findings

Key research contributions include:
- Novel multi-agent approaches to entity resolution
- Integration of graph databases with LLM reasoning
- Human-AI collaborative labeling systems
- Performance optimization techniques for large-scale entity matching

## Contributing

This is a personal research repository. If you're interested in collaboration or have suggestions:
1. Open an issue for discussion
2. Fork the repository for your own experiments
3. Submit pull requests for improvements

## License

This research code is provided for academic and research purposes. Please cite appropriately if used in publications.

## Contact

For questions about this research or potential collaborations, please open an issue in this repository.

---

*Last updated: September 2025*