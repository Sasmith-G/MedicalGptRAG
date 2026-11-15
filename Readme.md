# MedicalGPT RAG — Medical Question Answering with Knowledge Graphs

An AI-powered medical question-answering system that combines **Retrieval-Augmented Generation (RAG)** with **Knowledge Graphs** to provide context-aware responses to medical queries, supported by relevant medical information and source references.

The project explores how relationships between medical entities can improve information retrieval and provide more structured context than conventional document-based retrieval alone.

---

## Overview

Traditional Retrieval-Augmented Generation systems primarily retrieve information based on textual similarity. However, medical knowledge is highly interconnected: symptoms relate to diseases, diseases relate to treatments, and medications interact with other clinical concepts.

MedicalGPT RAG explores a graph-enhanced retrieval approach in which medical documents are processed into structured knowledge representations. Extracted entities and their relationships are used to construct a knowledge graph, which can then support retrieval during question answering.

The system provides a conversational interface where users can submit medical questions and receive generated responses accompanied by relevant references.

## Key Features

- **Medical Document Processing:** Breaks medical documents into smaller chunks for downstream processing.
- **Entity Extraction:** Identifies relevant medical concepts and entities from document content.
- **Relationship Extraction:** Connects related medical entities through structured relationships.
- **Knowledge Graph Construction:** Represents medical information through interconnected entities and relationships.
- **Graph-Based Retrieval:** Uses graph relationships to retrieve relevant context for incoming questions.
- **Context-Aware Question Answering:** Generates responses using retrieved medical information.
- **Source References:** Presents supporting references alongside generated responses.
- **Conversational Interface:** Provides an interface for interacting with the medical question-answering system.

## System Architecture

The system follows a document-processing and graph-enhanced retrieval workflow.

### 1. Document Processing

Medical documents are divided into smaller chunks. This makes the content easier to process and allows relevant sections to be retrieved during question answering.

### 2. Medical Entity Extraction

Relevant entities are extracted from the processed content. These may include:

- Diseases
- Symptoms
- Medications
- Treatments
- Medical procedures
- Clinical concepts

### 3. Relationship Extraction and Linking

Relationships between extracted entities are identified and represented as structured connections.

For example:

`Disease → has_symptom → Symptom`

`Drug → treats → Disease`

These relationships help represent the connections between different medical concepts.

### 4. Knowledge Graph Generation

Extracted entities and relationships are organised into a knowledge graph. The graph provides a structured representation of the medical information contained in the source documents.

### 5. Graph-Enhanced Retrieval

When a user submits a question, the retrieval pipeline identifies relevant medical information and uses the graph structure to explore related entities and relationships.

### 6. Response Generation

The retrieved context is used to generate a natural-language response. Supporting references are presented to help users trace the information back to its source.

## Architecture Diagram

![Medical Graph RAG Architecture](docs/images/medical-graph-rag-architecture.png)

*The diagram illustrates the document-processing pipeline, entity extraction, relationship linking, knowledge graph construction and graph-enhanced question-answering workflow.*

## Application Screenshots

### MedicalGPT Interface

![MedicalGPT Landing Page](docs/images/medicalgpt-home.png)

### Conversational Question Answering

![MedicalGPT Question Answering](docs/images/medicalgpt-chat.png)

### Knowledge Graph Processing

![Medical Knowledge Graph](docs/images/medical-graph-pipeline.png)

## How Graph RAG Differs from Conventional RAG

| Conventional RAG | Graph RAG |
|---|---|
| Primarily retrieves relevant text chunks | Can retrieve information through connected entities and relationships |
| Focuses on textual similarity | Incorporates structured relationships |
| Context is generally document-oriented | Context can include related concepts across documents |
| Useful for direct information retrieval | Useful when questions involve interconnected information |

The graph-based approach can provide additional context for questions that involve relationships between multiple medical concepts.

## Example Interaction

**User Query:**

"What are X-ray imaging methods primarily used for?"

**System Workflow:**

1. Receives the medical question.
2. Identifies relevant medical concepts.
3. Retrieves relevant information from the available knowledge sources.
4. Uses the retrieved context to generate an answer.
5. Presents the answer with supporting references.

## Technology Stack

The exact technologies should be listed after verifying the project source code.

- **Frontend:** [Confirm framework]
- **Backend:** [Confirm framework]
- **Programming Language:** [Confirm]
- **LLM Integration:** [Confirm provider/model]
- **Retrieval:** Graph-enhanced RAG
- **Knowledge Graph:** [Confirm graph database or graph representation]
- **Vector Storage:** [Confirm, if implemented]
- **Deployment:** [Confirm hosting platform]

## Project Structure

The repository is organised into separate frontend and backend components.

```text
MedicalGptRAG/
│
├── client/
│   └── Frontend application
│
├── server/
│   └── Backend application
│
├── docs/
│   └── images/
│       ├── medical-graph-rag-architecture.png
│       ├── medicalgpt-home.png
│       ├── medicalgpt-chat.png
│       └── medical-graph-pipeline.png
│
└── README.md
```

*The directory descriptions and documentation asset paths should be adjusted to match the actual repository.*

## Getting Started

### Prerequisites

Install the prerequisites required by the frontend and backend implementations.

- Git
- [Frontend runtime and package manager]
- [Backend runtime]
- Required database or graph storage service
- Required LLM/API credentials

### Installation

Clone the repository:

```bash
git clone https://github.com/Sasmith-G/MedicalGptRAG.git
cd MedicalGptRAG
```

### Frontend Setup

```bash
cd client
# Install dependencies using the package manager specified by the project
# Start the frontend using its configured development command
```

### Backend Setup

```bash
cd server
# Install backend dependencies
# Configure environment variables
# Start the backend using its configured entry point
```

### Environment Configuration

Create the environment files required by the application and configure the credentials for the services it actually uses.

Do not commit API keys, database credentials, or other secrets to the repository.

## Use Cases

- Exploring medical information through natural-language questions.
- Retrieving context from medical documents.
- Understanding relationships between medical concepts.
- Accessing supporting references for generated answers.
- Exploring the application of Knowledge Graphs in medical information retrieval.

## Limitations and Responsible Use

This project is an educational and technical exploration of AI-powered medical information retrieval.

- Generated responses may contain inaccuracies or incomplete information.
- Retrieved references should be independently checked.
- The system is not a substitute for professional medical advice, diagnosis or treatment.
- It should not be used for emergency medical decisions.
- Clinical reliability, regulatory compliance and medical validation must not be assumed without formal evaluation.

## Research Reference

This project explores concepts related to:

**Medical Graph RAG**

Research paper: https://arxiv.org/pdf/2408.04187

## Acknowledgements

This project is based on the original implementation and research inspiration from its original author.

Original repository: https://github.com/Sasank-V/MedicalGraphRAG

The original author and applicable licensing information should be retained and acknowledged.

---

**MedicalGPT RAG — Exploring the intersection of Medical AI, Knowledge Graphs and Retrieval-Augmented Generation.**
