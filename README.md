Adaptive RAG is a fascinating technology that picks the best retrieval-augmented generation strategy based on the complexity of your queries. It’s like having a smart assistant that always knows the best way to find and present information.
Here’s a README file for your demo on setting up an adaptive RAG system that routes queries based on complexity into various pipelines:

---

# Adaptive Retrieval-Augmented Generation (RAG) Demo

This repository demonstrates an adaptive Retrieval-Augmented Generation (RAG) system that dynamically routes user queries based on their complexity into different pipelines. The adaptive RAG framework enhances response accuracy by selecting the appropriate strategy for handling queries, ensuring efficient processing for both simple and complex requests.

## Table of Contents
1. [Introduction](#introduction)

2. [Installation](#installation)

3. [How It Works](#how-it-works)

4. [Contributing](#contributing)


## Introduction
Retrieval-Augmented Large Language Models (LLMs) integrate non-parametric knowledge from external databases into LLMs to enhance response accuracy for various tasks, especially Question-Answering (QA). This approach, however, can suffer from inefficiencies when dealing with queries of varying complexity.

In this demo, we propose an **adaptive RAG framework** capable of dynamically selecting the most suitable strategy for LLMs, ranging from simple retrieval-augmented LLM methods to more complex multi-step pipelines, based on query complexity. 


## Installation

To set up the adaptive RAG system, follow these steps:

1. **Clone the repository**:
    ```bash
    git clone https://github.com/Aaryaveerkrishna23/adaptive_rag.git
    cd adaptive_rag
    ```
    
2. **Set up API keys**:
   - Ensure you have access to an LLM API (e.g., OpenAI, Google Gemini) and external retrieval resources. Add your API keys in the configuration files.



## How It Works

1. **Query Classification**:
    - Incoming queries are first passed through the **Semantic Router**, which routes the query based upon it's complexity. 

2. **Pipeline Selection**:
    - Based on the classification, the system selects one of three pipelines:
        - **Simple Pipeline**: For quick and easy queries.
        - **Iterative Pipeline**: For queries that require complex, multi-step responses.
        - **No-Retrieval Pipeline**: For cases where no external information is necessary.

3. **Query Processing**:
    - The selected pipeline processes the query and returns a response.

## Contributing

We welcome contributions to enhance this demo and improve the adaptive RAG framework. Please feel free to submit pull requests or open issues for discussion.


### Example Query Flow:

- **Simple Query**: "What is the capital of India?"
  - Routed to Simple Pipeline.
  - Response: "New Delhi."

- **Complex Query**: "Can you explain the evolution of computer networks from the 1960s to today?"
  - Routed to Iterative Pipeline.
  - Response: A detailed multi-step response covering different eras.

