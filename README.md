# Nirmaya AI V2

<p align="center">
  <img src="https://readme-typing-svg.demolab.com?font=Inter&weight=600&size=30&duration=3000&pause=900&color=0F766E&center=true&vCenter=true&width=850&lines=Nirmaya+AI+V2;AI-Powered+Healthcare+Technology;Building+Intelligent+Retrieval+Systems" alt="Nirmaya AI V2 animated title" />
</p>

<p align="center">
  <strong>Engineering a scalable foundation for AI-assisted healthcare information workflows.</strong>
  <br />
  <sub>Version 2 · AI Infrastructure · Cloud Engineering</sub>
</p>

<p align="center">
  <img alt="License" src="https://img.shields.io/badge/License-MIT-0F766E.svg" />
  <img alt="Status" src="https://img.shields.io/badge/Status-Under%20Development-64748b.svg" />
</p>

---

## Overview

Nirmaya AI V2 is an early-stage project for exploring AI-assisted healthcare document workflows and information retrieval. The product direction mentions document processing, semantic search, and context-aware AI experiences.

> **Current repository status:** this is a documentation scaffold. It contains a README and MIT license, but no running application, dependencies, database schema, cloud infrastructure, or AI integration. AWS, Amazon Bedrock, vector search, and PostgreSQL are named in the project brief as intended technologies; no implementation of them is present here.

## Contents

- [Engineering principles](#engineering-principles)
- [Project status](#project-status)
- [Architecture concept](#architecture-concept)
- [Technology direction](#technology-direction)
- [AI, embeddings, and retrieval](#ai-embeddings-and-retrieval)
- [Data and document lifecycle](#data-and-document-lifecycle)
- [Repository layout](#repository-layout)
- [Local setup](#local-setup)
- [Configuration and developer commands](#configuration-and-developer-commands)
- [Security and privacy](#security-and-privacy)
- [Deployment and operations](#deployment-and-operations)
- [Roadmap](#roadmap)
- [Contributing](#contributing)
- [License](#license)

## Engineering principles

These principles describe the intended direction for implementation:

- **Modularity:** define clear boundaries between user experience, APIs, data, and AI services.
- **Data integrity:** make persistence and document lifecycle explicit and reviewable.
- **Grounded AI:** design retrieval and source tracking so responses can be evaluated against their inputs.
- **Security by design:** plan for least-privilege access, secret handling, and data isolation before sensitive data is introduced.
- **Operability:** include observability, recovery, and cost controls when infrastructure is selected.

## Project status

| Area | Evidence in this repository | Status |
| --- | --- | --- |
| Application | No frontend, backend, worker, or API source files | Not implemented |
| AWS and Bedrock | No SDK configuration, model IDs, or infrastructure definitions | Not verified or configured |
| Embeddings and vector search | No embedding code, index, or retrieval implementation | Not implemented |
| PostgreSQL | No connection settings, schema, ORM models, or migrations | Not implemented |
| Developer tooling | No dependency manifest, test suite, or build configuration | Not present |
| License | Root `LICENSE` file | MIT |

The tracked repository consists of `README.md` and `LICENSE`. Update this table and the setup instructions as implementation is added.

## Architecture concept

The diagram is a **proposed concept**, not a deployed or implemented architecture. Dashed arrows show possible future interactions. Storage, vector search, model inference, and service boundaries remain undecided.

```mermaid
flowchart LR
    U[User] -. future use .-> FE[Frontend]
    FE -. request .-> API[Backend API]
    API -. metadata .-> DB[(PostgreSQL, proposed)]
    API -. submit document .-> ING[Ingestion and processing]
    ING -. original files .-> STORE[Document storage, undecided]
    ING -. vectors .-> IDX[Vector search, undecided]
    API -. query and context .-> RET[Retrieval orchestration]
    IDX -. matching passages .-> RET
    RET -. prompt .-> MODEL[Foundation model, undecided]
    MODEL -. response .-> API
```

No queues, network topology, failure handling, or authorization flow can be verified yet. An implementation should define component ownership, check access before retrieval, handle partial failures and retries, and retain enough source information to inspect how a response was produced.

## Technology direction

The project brief names AWS, Amazon Bedrock, vector search, and PostgreSQL as intended technologies. The repository does not confirm a specific cloud service, database product, or application framework. In particular, there is no evidence here of S3, OpenSearch, Aurora, RDS, Lambda, ECS, EKS, or any other named AWS service.

No AWS region, IAM role, credential method, network policy, or encryption configuration is defined. Record selected services and their operational responsibilities when they are implemented; do not treat this section as a deployment inventory.

## AI, embeddings, and retrieval

No foundation model or embedding model identifiers, inference calls, prompt templates, token limits, retries, or response validation are present. It is not possible to confirm whether future inference or embedding generation will use Bedrock or another provider.

There is no chunking policy, embedding dimension, vector index, similarity metric, metadata filter, retrieval access control, or source attribution implementation. Retrieval-augmented generation (RAG), citations, and grounded responses are not available capabilities at this stage.
