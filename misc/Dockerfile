FROM python:3.11-slim

RUN apt-get update && \
    apt-get install -y --no-install-recommends procps && \
    rm -rf /var/lib/apt/lists/*

RUN pip install --trusted-host pypi.org --trusted-host pypi.python.org --trusted-host=files.pythonhosted.org --upgrade --force-reinstall pip --break-system-packages

RUN pip install --trusted-host pypi.org --trusted-host pypi.python.org --trusted-host=files.pythonhosted.org --upgrade --force-reinstall openai python-dotenv requests --break-system-packages

WORKDIR /llm-connector

#keep the container running after start
CMD ["python3", "-c", "import time; exec('while True:\\n time.sleep(300)')"] 
