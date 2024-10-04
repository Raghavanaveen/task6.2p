# Dockerfile for book_catalog microservice
FROM python:3.9-slim

WORKDIR /book_catalog

COPY book_catalog/requirements.txt /book_catalog/requirements.txt

RUN pip install --no-cache-dir -r requirements.txt

COPY book_catalog /book_catalog

EXPOSE 8000

ENV DATABASE_URL="postgresql://raghava_task6_2p_user:yCatT4SeB4huzmOwCvkK5XyeT06EqDfC@dpg-crvp8l5ds78s738adcvg-a.oregon-postgres.render.com/raghava_task6_2p"

CMD ["uvicorn", "main:app", "--host", "0.0.0.0", "--port", "8000"]