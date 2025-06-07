FROM python:3.11.9-slim

COPY requirements.txt requirements.txt
RUN pip install -r requirements.txt

COPY . .
COPY entrypoint.sh /entrypoint.sh
RUN apk add --no-cache netcat-openbsd
RUN chmod +x /entrypoint.sh
CMD ["/entrypoint.sh"]
