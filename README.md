# Langchain Chatbot for Multiple PDFs

Langchain Chatbot App is a Python application that enables a personal chat experience
with your data that includes proprietary data. The Langchain chatbot queries
information from multiple PDF documents. The Langchain chatbot is built using OpenAI API and free 
Large Language Models (LLMs)

## Introduction: 

Data is everywhere. Countless PDFs sit on our personal computers.
The information contained in PDF documents often poses a challenge when trying to 
retrieve specific information. Langchain Chatbot, a personal chatbot application built 
using OpenAI API and LLMs, transforms the way we interact with PDF content. By seamlessly
integrating natural language processing and machine learning techniques, the Langchain 
chatbot offers a powerful conversational interface for querying information from multiple 
PDFs.

### High-Level Workflow: An overview of how to use Langchain to chat with your data.
The components that are involved in semantic search.
![Hight-Level](https://github.com/preethichan/PersonalChatbot/blob/main/docs/RAG.jpg)


### Use Case: Business

1. streamline the information retrieval process.
2. Quick and accurate access to crucial information.
3. Save time and resources.

### How it Works
![img.png](https://github.com/preethichan/PersonalChatbot/blob/main/docs/PDF-LangChain.jpg)

The above architecture shows us the sequence of steps that 
are performed for the application to run. 
1. PDF Loading- We use Langchains document loader functions to 
   import multiple PDF files. 
2. Text Splitting- We split the loaded text into semantically meaningful 
   chunks. There are several types of splitters. However, we use characterTextSplitter
   to split text that looks at characters.
3. Vectorstores and Embedding- storing the chunks into an index using
   vector stores and embedding. Embedding takes a piece of text and creates
   a numerical representation of that text. Text with similar content
   will have similar vectors in numeric space. Vector store is a database to
   look up similar vectors white retrieval.
4. Language Model- The application utilizes a Large Language model to generate
   vector representation(embeddings) of the text chunks.
5. Similarity Matching- When the user asks the question, the app compares it with the text 
   chunks and identifies the most semantically similar ones.
6. Response Generation- The selected chunks are passed to the language mode LLM, which
   generates a response based on the relevant content of the PDFs.

### Dependencies and Installation

To install the Langchain Chatbot App, Follow these steps:
1. Clone the repository to your local machine.
2. Install the required dependencies by running the following command
   `pip install -r requirements.txt`
3. Create a Virtual Environment using the following command:
  ` pip install virtualenv
    python<version> -m venv <virtual-environment-name>
    <virtual-environment-name>\Scripts\activate`
4. Obtain an API key from OpenAI and add it to the .env file in the project directory.
   OPENAI_API_KEY="<your key>"
5. Run the App:
   `streamlit run app.py`

### Application Usage and Output: 
1. Upload Documents Here: Use browse files or drag and drop the pdf files.
2. Ask anything to your PDF: Use the chat interface to enter your questions related to
   the content of the uploaded PDFs.
3. Interactive responses: The chatbot will generate responses based on the information retrieved
   from the PDFs.

![img_2.png](https://github.com/preethichan/PersonalChatbot/blob/main/docs/Output.png)https://github.com/preethichan/PersonalChatbot/blob/main/docs/Output.png)
 
