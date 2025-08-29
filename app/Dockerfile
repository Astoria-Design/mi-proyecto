FROM python:3.12-slim

WORKDIR /app

COPY requirements.txt .
RUN pip install --no-cache-dir -r requirements.txt

COPY ./app /app

EXPOSE 8000

CMD ["gunicorn", "mi_proyecto.wsgi:application", "--bind", "0.0.0.0:8000"]
