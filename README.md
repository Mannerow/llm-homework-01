# llm-homework-01

## 📝 Description

The repository facilitates the retrieval and search of course-related FAQ documents, using them to construct detailed prompts for OpenAI's model. It starts by using the `requests` library to download JSON-formatted documents from GitHub, then enriches and indexes these documents in Elasticsearch with the `elasticsearch` Python library for advanced querying capabilities. The data is processed and indexed to allow for efficient searches tailored to specific questions and contexts. Once relevant FAQs are retrieved, the repository uses these details to build structured prompts, which are then submitted to OpenAI’s model to generate comprehensive and contextually relevant answers. This integration provides a streamlined approach to generating precise responses based on the FAQs, leveraging both Elasticsearch's powerful search capabilities and OpenAI's advanced language model.

## 🔧 Instructions to Run

In a seperate terminal, run elasticsearch with docker: 

```bash
docker run -it \
    --rm \
    --name elasticsearch \
    -p 9200:9200 \
    -p 9300:9300 \
    -e "discovery.type=single-node" \
    -e "xpack.security.enabled=false" \
    docker.elastic.co/elasticsearch/elasticsearch:8.4.3
```

Install pipenv and activate the shell:

```bash
# Install pipenv
pip install pipenv

# Create a new pipenv environment or activate an existing one
pipenv shell
```

Create a new file named .envrc

```bash
touch .envrc
```

Add your OPENAI_API_KEY to the file: 

```bash
export OPENAI_API_KEY="<your-openai-api-key>"
```

To ensure that your environment variable is recognized, you need to either source the .envrc file manually or use a tool like direnv to load it automatically:

```bash
direnv allow
```

Run the jupyter notebook file: 'search.ipynb'