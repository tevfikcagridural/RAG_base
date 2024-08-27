# Retrieval-Augmented Generation (RAG) System Structure
Inspired from [cookie-cutter-data-science](https://cookiecutter-data-science.drivendata.org).

This work suggests an overview of how to structure a directory for a Retrieval-Augmented Generation (RAG) system. The proposed structure is designed to organize the various components and workflows typically involved in developing and maintaining the system.

## Project Structure

```sh
rag-app/
├── data/                           # Only some samples. **It is recommended to separate data stores/databases from codebase**
│   ├── raw/                        # Raw, unprocessed data files
│   ├── evaluation                  # Evaluation data files
│   ├── processed/                  # Data files after processing
│   └── external/                   # External data sources
├── models/                         # For using local models 
│   ├── embeddings/                 # Pretrained/fine-tuned embedding model(s)
│   └── llm/                        # Pretrained/fine-tuned language model(s)
├── prompts/            
│   ├── prompt1.txt                 # Sample prompt file
│   ├── prompt2.txt                 # Another sample prompt file
├── reports/
│   ├── development_report.md       # Reports on experiments and/or analyses
│   └── figures/                    # Figures for reports
├── src/                            # Main source code of the application.
│   ├── data/
│   │   └── data_preparation.py     # Data preparation scripts
│   ├── models/
│   │   ├── embedding_models.py     # Embedding model(s) handling
│   │   └── llm_models.py           # Language model(s) handling
│   ├── services/
│   │   └── inference_service.py    # Data loading, indexing, and storing embeddings to vector database.
│   │   └── ingestion_service.py    # Retrieval and generation.
│   │   └── monitoring_service.py   # Monitoring service of the RAG system
│   └── app/                        # Main application entry point
│       └── main.py                 
├── tests/
│   ├── __init__.py
│   ├── test_data_preparation.py    # Unit tests for data preparation
│   ├── test_embedding_model.py     # Unit tests for embedding model
│   ├── test_llm_model.py           # Unit tests for language model
│   └── test_rag_service.py         # Unit tests for RAG services
├── notebooks/
│   └── data_exploration.ipynb      # Jupyter notebook for data exploration and analysis
│   ├── experiments.ipynb           # Jupyter notebook for experiments on different strategies
├── docker/                         # For containerized deployment 
│   ├── Dockerfile                  # Dockerfile for building the image
│   └── docker-compose.yml          # Docker Compose file for multi-container setups
├── .env                            # Environment variables
├── README.md                       # Project README file
├── requirements.txt                # Python dependencies
```

Contact c.dural@gmail.com