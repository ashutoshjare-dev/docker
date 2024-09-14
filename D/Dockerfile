FROM python:3.8-alpine
ENV PYTHONUNBUFERED=1
RUN apk update && apk add postgresql-dev gcc python3-dev musl-dev
WORKDIR /django
COPY requirements.txt requirements.txt
RUN pip install -r requirements.txt
COPY . .
CMD [ "python3", "manage.py", "runserver", "0.0.0.0:8000" ]
