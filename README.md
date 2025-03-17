# Medical-Assistant-Chatbot-RAG
This is a Streamlit-based Medical Assistant Chatbot that leverages FAISS for vector storage and Hugging Face models for natural language processing. The chatbot provides answers based on a given knowledge base and does not generate responses beyond the provided context.

## **Features**

- Uses FAISS for efficient similarity search and retrieval.

- Embeds text using Hugging Face's sentence-transformers/all-MiniLM-L6-v2.

- Utilizes Mistral-Nemo-Instruct-2407 from Hugging Face for answering queries.

- Implements custom prompt engineering for better context-based responses.

- Supports interactive chat interface using Streamlit.
## **Installation**
1-Create a virtual environment and install dependencies:
```sh
python -m venv venv
source venv/bin/activate  
pip install -r requirements.txt
```
2-Set up environment variables:

Create a .env file in the project root and add your Hugging Face API token:
```sh
HF_TOKEN=your_huggingface_api_key
```
3-Run the Streamlit app:
```sh
streamlit run app.py
```
## **Usage**

- Open the Streamlit UI in your browser.

- Enter your medical-related query in the chat input box.

- The chatbot will retrieve relevant information and respond based on the knowledge base.
## **Project Structure**
```"plaintext"
medical-chatbot/
│── vectorstore/             # FAISS vector database
│── app.py                   # Main Streamlit application
│── requirements.txt         # Required Python packages
│── .env                     # Environment variables 
│── README.md                # Documentation
```
## **Key Components**

- get_vectorstore(): Loads the FAISS vector database with embeddings.

- set_custom_prompt(): Defines a structured prompt template.

- load_llm(): Loads the Hugging Face model with a specified API token.

- main(): Runs the Streamlit chatbot interface.

## **Troubleshooting**

- FAISS vector store not found? Ensure the vector database is generated and placed in vectorstore/db_faiss.

- Invalid Hugging Face token? Verify that your .env file contains the correct API key.

- Model not responding? Check for typos in the Hugging Face repo ID and API token.

## **License**

This project is licensed under the MIT License.
