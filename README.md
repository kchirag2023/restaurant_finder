# Restaurant Finder

Restaurant finder is AI bot , created to find info about various restaurant and its menu using Azure OpenAI and Azure Cosmo DB for mongoDB

## Installation



```bash
pip install -r requirements.txt
```

## To run a project



```bash
cd vectorize.py
```
```bash
streamlit run vectorize.py
```

# Exploring different files of the project

## open_ai.py
This file contains a Python script that demonstrates how to integrate Azure OpenAI's chat capabilities using the AzureOpenAI Python SDK. The chatbot interacts with users, responding to queries related to a fictional bicycle and bicycle accessories store named Cosmic Works.


Environment Setup: The script uses dotenv to load environment variables (AOAI_ENDPOINT and AOAI_KEY) from a .env file, ensuring secure API authentication.

AzureOpenAI Integration: It initializes an instance of AzureOpenAI using the endpoint and API key retrieved from the environment variables.

Chatbot Interaction: The chatbot model "gpt-35-turbo" is used to simulate conversations.



## db.json
This file contains json data which model uses to interact with user.



## cosmodb.py
This file contains a Python script designed to import JSON data into a MongoDB database using the pymongo library. The script connects to a MongoDB instance specified in the environment variables, loads JSON data from a file, and inserts it into a predefined collection within the database.

Key Components:
Environment Setup: The script uses dotenv to load environment variables (DB_CONNECTION_STRING) from a .env file, ensuring secure connection details for MongoDB.

MongoDB Connection: It establishes a connection to MongoDB using the pymongo.MongoClient with the connection string retrieved from the environment variables.

Data Import: JSON data is read from a local file (db.json) using Python's json module. The script then inserts this data into a MongoDB collection (restaurants in the restro database).

## vectorize.py
This repository contains a Streamlit-based Python script designed to create a restaurant finder application. The application integrates MongoDB for data storage and Azure OpenAI for natural language processing capabilities. It allows users to ask questions about restaurants and receive relevant information based on stored data.

### Key Features:
Environment Setup: The script uses dotenv to load environment variables from a .env file, including MongoDB connection details (DB_CONNECTION_STRING) and Azure OpenAI credentials (AOAI_ENDPOINT and AOAI_KEY).

### Backend Integration:

MongoDB: Establishes a connection to MongoDB (restro database) using pymongo. It includes functions to import JSON data (db.json) into the restaurants collection and to add vectorized content fields using Azure OpenAI for similarity search.

Azure OpenAI: Utilizes the Azure OpenAI API (AzureOpenAI client) for generating embeddings from text (generate_embeddings function) and conducting conversational AI using the RAG model (rag_with_vector_search function).

### Frontend UI (Streamlit):

User Input: Provides an input field (st.text_input) for users to ask questions about restaurants.

Bot Response: Displays responses (st.write) generated by the RAG model based on user queries. It simulates restaurant information retrieval and interaction.

Interaction: Includes a button (st.button) to submit user questions and retrieve corresponding bot responses.

## To run a project



```bash
cd vectorize.py
```
```bash
streamlit run vectorize.py
```


## Contributor

👋 Hi, I'm Kumar Chirag! 🚀

I'm a student and developer with a keen interest in new technology. I'm passionate about exploring everything the world of technology has to offer!


## License

[MIT](https://choosealicense.com/licenses/mit/)
