FROM python:3.11.9-slim

ENV BOT_TOKEN=8085541907:AAFTLunIk6dcmFXYUoKP88GkkKGvk5wtYe0

COPY requirements.txt requirements.txt
RUN pip install -r requirements.txt

COPY . .

CMD ["sh", "-c", "alembic upgrade head && python bot.py & python main.py"]
