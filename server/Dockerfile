FROM python:3.11.9-slim

COPY requirements.txt requirements.txt
RUN pip install -r requirements.txt

COPY . .
COPY entrypoint.sh /entrypoint.sh
RUN apt-get update && apt-get install -y netcat && rm -rf /var/lib/apt/lists/*
RUN chmod +x /entrypoint.sh
CMD ["/entrypoint.sh"]
