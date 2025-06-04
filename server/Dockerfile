FROM python:3.11.9-slim

ENV BOT_TOKEN=8085541907:AAFTLunIk6dcmFXYUoKP88GkkKGvk5wtYe0
ENV FLOWER_MONITORING_DBNAME=flower_monitoring
ENV FLOWER_MONITORING_HOST=localhost
ENV FLOWER_MONITORING_PASSWORD=user
ENV FLOWER_MONITORING_USER=flower_user

COPY requirements.txt requirements.txt
RUN pip install -r requirements.txt

COPY . .

CMD ["sh", "-c", "alembic upgrade head && python bot.py & python main.py"]
