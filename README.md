# Multi AI RAG Chatbots Using Langgraph And AstraDB

## Overview

This project demonstrates the creation of an multi AI agent application using Langgraph and AstraDB. The application is designed to handle user queries by routing them to either a vector database (AstraDB) or an external tool like Wikipedia search, based on the nature of the query. The system leverages Langgraph for managing the state and communication between agents, and AstraDB for storing and retrieving vectorized data.

## Project Structure

- **Jupyter Notebook**: `Multi_AI_RAG_Chatbots_Using_Langgraph_AstraDB.ipynb`
- **Dependencies**: Langchain, Langgraph, AstraDB, Hugging Face embeddings, Grok API, Wikipedia API

## Key Features

1. **Multi-Agent Communication**: The application uses Langgraph to manage multiple AI agents that communicate with each other and handle different tasks.
2. **State Management**: Langgraph helps in managing the state of the agents, ensuring smooth communication and workflow.
3. **Vector Database**: AstraDB is used to store and retrieve vectorized data, enabling efficient querying and retrieval.
4. **External Tool Integration**: The system integrates with external tools like Wikipedia search to handle queries that cannot be fulfilled by the vector database.
5. **Prompt Engineering**: The application uses prompt engineering to guide the LLM (Language Model) in generating appropriate responses.

## Architecture

The architecture of the project can be summarized as follows:

1. **Start Node**: The workflow begins with a start node that receives the user query.
2. **Router**: The router determines whether the query should be routed to the vector database or an external tool like Wikipedia search.
3. **Vector Database (AstraDB)**: If the query is related to the topics stored in the vector database (e.g., agents, prompt engineering, adversarial attacks), it is routed here.
4. **External Tool (Wikipedia Search)**: If the query is not related to the topics in the vector database, it is routed to Wikipedia search.
5. **LLM Integration**: The responses from the vector database or Wikipedia search are integrated with the LLM for final processing and response generation.
6. **End Node**: The final response is returned to the user.

## Implementation Steps

### 1. Setting Up AstraDB

- **Create AstraDB**: Sign in to AstraDB and create a serverless vector database.
- **Generate Tokens**: Create and manage tokens for accessing the AstraDB.

### 2. Installing Dependencies

- Install necessary libraries such as Langchain, Langgraph, and Hugging Face embeddings.
- Install additional libraries for external tool integration (e.g., Wikipedia API).

### 3. Data Ingestion

- **Web Scraping**: Read data from specified URLs and convert it into vectors.
- **Vectorization**: Use Hugging Face embeddings to convert text data into vectors.
- **Storing Vectors**: Store the vectorized data in AstraDB.

### 4. Building the Langgraph Application

- **Define Data Model**: Create a data model to manage the state of the graph.
- **Retrieve Function**: Define a function to retrieve data from the vector database.
- **Wikipedia Search Function**: Define a function to query Wikipedia.
- **Router Function**: Define a router function to determine the data source (vector database or Wikipedia).
- **Graph Construction**: Build the Langgraph workflow by defining nodes and edges.
- **Conditional Logic**: Add conditional logic to route queries based on the router function.

### 5. Execution and Testing

- **Compile the Graph**: Compile the Langgraph application.
- **Execute Queries**: Test the application by executing various queries and observing the responses.

## Example Queries

- **Query**: "What is an agent?"
  - **Response**: Routes to the vector database and retrieves relevant information.
- **Query**: "Who is Robert Knepper?"
  - **Response**: Routes to Wikipedia search and retrieves relevant information.

## Conclusion

This project showcases the power of combining Langgraph and AstraDB to create a robust, multi AI agent application. The system efficiently handles user queries by leveraging a vector database for specific topics and external tools like Wikipedia for general queries. The use of Langgraph ensures seamless state management and communication between agents, making the application highly scalable and flexible.

## Next Steps

- **Enhance External Tool Integration**: Explore and integrate more external tools to handle a wider range of queries.
- **Optimize Vector Database**: Experiment with different vectorization techniques and database configurations to improve retrieval efficiency.
- **Expand Data Sources**: Incorporate additional data sources to enrich the vector database.

## References

- [Langchain Documentation](https://langchain.readthedocs.io/)
- [Langgraph Documentation](https://langgraph.readthedocs.io/)
- [AstraDB Documentation](https://docs.datastax.com/en/astra/docs/)
- [Hugging Face Embeddings](https://huggingface.co/docs/transformers/main/en/model_doc/bert)
- [Grok API](https://grok.com/)
- [Wikipedia API](https://www.mediawiki.org/wiki/API:Main_page)

---
