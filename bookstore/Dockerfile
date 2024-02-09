FROM python:3.11

ENV PYTHONDONTWRITEBYTECODE 1
ENV PYTHONUNBUFFERED 1

WORKDIR /app

ADD . /app/

RUN apt-get update && \
    apt-get install -y && \
    pip install --upgrade pip && \
    pip install --no-cache-dir --upgrade -r requirements.txt

EXPOSE 8000

CMD ["python", "manage.py", "runserver", "0.0.0.0:8000"]
    
