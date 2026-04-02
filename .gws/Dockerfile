FROM mirror.gcr.io/library/python:3.11-slim

ENV PYTHONUNBUFFERED=1 \
    PYTHONDONTWRITEBYTECODE=1 \
    PIP_NO_CACHE_DIR=1

WORKDIR /app


COPY requirements.txt .
RUN pip install --upgrade pip && pip install -r requirements.txt

COPY main.py .


EXPOSE 8000

CMD ["sanic", "main:app", "--host=0.0.0.0", "--port=8000", "--dev"]
