** LLM RAG 
   Search documents using Elastic Search and openai
 Chat with your own data **

** You need:
Docker
Python 3.10
OpenAI account
**

We will use pipenv for dependency management. Let's install it:
pip install pipenv

#Install the packages
pipenv install tqdm notebook==7.1.2 openai elasticsearch

Start a new terminal, and there run jupyter:

pipenv run jupyter notebook

In another terminal, run elasticsearch with docker:

docker run -it \
    --name elasticsearch \
    -p 9200:9200 \
    -p 9300:9300 \
    -e "discovery.type=single-node" \
    -e "xpack.security.enabled=false" \
    docker.elastic.co/elasticsearch/elasticsearch:8.4.3

Verify that ES is running

curl http://localhost:9200

1- First, we need to download the docs:

wget https://github.com/alexeygrigorev/llm-rag-workshop/raw/main/notebooks/documents.json

2- Load and Seach teh Document

3- We need to create an Elastic Search index

4- Create a opeai client connection

5- Create prompt using our question and Elastic documents

6- Get reposnse from openai
