# N8N Starter

Following the structure here: https://github.com/n8n-io/self-hosted-ai-starter-kit

Included a python script to convert pdfs to markdown, which can then be read into to Qdrant.

Another workflow will allow you to chat with Qdrant.

# Steps to run

1. Create a virtual environment `python -m venv env`
2. Activate virtual environment `source env/bin/activate`
3. Install requirements `pip install -r requirements.txt`
4. Setup `.env` file with the following:
```
NODE_ENV=production
WEBHOOK_URL=http://localhost:5678
DB_TYPE=postgresql
DB_POSTGRES_HOST=postgres
DB_POSTGRES_PORT=5432
DB_POSTGRES_DATABASE=n8n
DB_POSTGRES_USER=n8n
DB_POSTGRES_PASSWORD=
QDRANT_HOST=qdrant
QDRANT_PORT=6333
POSTGRES_DB=n8n
POSTGRES_USER=n8n
POSTGRES_PASSWORD=
QDRANT__SERVICE__GRPC_PORT=6334
QDRANT__SERVICE__HTTP_PORT=6333
```
Set your own passwords and users
5. `docker compose up -d`


This assumes you have ollama already installed.  The n8n nodes will need to be configured with your own credentials.
