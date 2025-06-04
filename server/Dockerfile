FROM python:3.11.9-slim

ENV BOT_TOKEN=8085541907:AAFTLunIk6dcmFXYUoKP88GkkKGvk5wtYe0
ENV FLOWER_DATABASE_URL mysql+asyncmy://flower_user:user@localhost:3306/flower_monitoring

COPY requirements.txt requirements.txt
RUN pip install -r requirements.txt

COPY . .

CMD ["sh", "-c", "alembic upgrade head && python bot.py & python main.py"]
