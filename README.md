# LangFlow Template: Vector Store with Pinecone and OpenAI Integration

## Overview
This LangFlow template provides an end-to-end pipeline for managing user inputs, generating embeddings with Hugging Face, storing them in Pinecone, and utilizing OpenAI for LLM-based responses. The flow consists of several components, including vector stores, embeddings, prompts, and data manipulation tools, aimed at efficiently processing and querying data.

## Components

- **Chat Input:**  
  The starting point for the flow. Accepts user input messages for processing.

- **HuggingFace Embeddings:**  
  Utilizes the Hugging Face inference API (`sentence-transformers/all-MiniLM-L6-v2`) to generate embeddings from text. These embeddings represent the input data in a vector space.

- **Pinecone Vector Store:**  
  A powerful vector database that stores embeddings generated by Hugging Face. It supports querying and searching across vectors for retrieval tasks.

- **Prompt:**  
  Creates a template prompt with dynamic variables to query the language model.

- **OpenAI (ChatGPT):**  
  Sends the dynamic prompt to OpenAI’s GPT models, generating a relevant response based on the given query.

- **Parse Data:**  
  Converts the text data to plain text following a specified structure for further processing.

- **Split Text:**  
  Splits the input text into smaller chunks based on a delimiter, making the data easier to manage.

- **File Loader:**  
  A generic file loader component that can load external data, such as documents, into the flow for processing and embedding.

- **Output:**  
  Displays the final chat message generated by the pipeline in the Playground for review.

## Flow Description

1. **User Input:**  
   The flow begins with the user entering a query or message.

2. **Embedding Generation:**  
   The text input is sent to the HuggingFace Embeddings component, which generates an embedding representing the message in vector form.

3. **Vector Storage:**  
   The embedding is stored in Pinecone for efficient querying later. This helps in tasks like searching for similar entries.

4. **Dynamic Prompt:**  
   Based on the user’s message and embedding, the system creates a dynamic prompt that is tailored to interact with the language model.

5. **OpenAI Query:**  
   The dynamic prompt is sent to OpenAI’s GPT-3.5/4 for generating a natural language response.

6. **Display Output:**  
   The response is then displayed in the Playground as output.

## How to Use

1. **Clone this repository** to your local machine.

2. **Install Dependencies:**  
   Make sure you have the following dependencies installed:
   - LangFlow
   - Pinecone
   - Hugging Face API
   - OpenAI API

3. **Configure APIs:**
   - HuggingFace API key is required for generating embeddings.
   - Pinecone API key and environment need to be set up to manage the vector store.
   - OpenAI API key is required for interacting with GPT models.

4. **Run the Project:**  
   Open LangFlow and load this template. Interact with the flow by entering text in the Chat Input component and observing the results in the Output.

## Future Enhancements

- Integration of additional embedding models.
- Enhanced query capabilities using more advanced Pinecone features.
- Fine-tuned prompt templates for domain-specific use cases.

---

![LangFlow Template](https://github.com/user-attachments/assets/f42dd2cb-e638-4ce2-8101-ac69cc641b83)

