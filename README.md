# DirectoryGPT

## Introduction
DirectoryGPT is an large language model fine tuned to documents in directory data uploads. Users have the option to utilize enterprise or open-source language models.
Note: Utilizing the open-source LLM requires 3-8GB of storage and at least 9.82GB RAM.

## Process Flow 
1. Vectorstore creation to tokenize directory's documents
2. Direct use from Python script OR Flask API use
- Currently only POST requests are allowed. DELETE is in development.

## Requirements
1. OpenAI API Key: for enterprise LLM
2. MongoDB Cluster: [More Information Here](https://www.mongodb.com/basics/clusters/mongodb-cluster-setup)

## Set up
1. Route the desired relative directory in ln 83 of [create_vectorstore_from_directory](create_vectorstore_from_directory.py)
2. Designate the name of chromadb folder in ln 84 of [create_vectorstore_from_directory](create_vectorstore_from_directory.py)
3. If using as API, from 2, change the relative import folder in ln 35 of [use_chatbot_api](use_chatbot_api.py)


## GPT4All Configuration
- Model used: [nous-hermes-13b.ggmlv3.q4_0.bin](https://huggingface.co/TheBloke/Nous-Hermes-13B-GGML/tree/main)

## Other Notes
1. To use a different model within GPT4All, add bin file to model folder.


