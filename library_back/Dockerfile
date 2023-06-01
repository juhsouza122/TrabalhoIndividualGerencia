FROM python:latest
WORKDIR /app
COPY ./ ./

ENV POSTGRES_DB=library_db
ENV POSTGRES_USER=postgres
ENV POSTGRES_PASSWORD=postgres
ENV POSTGRES_HOST=db
ENV POSTGRES_PORT=5432

RUN python3 -m pip install -r requirements.txt
EXPOSE 8000
CMD python3 manage.py makemigrations ; python3 manage.py migrate ; python3 manage.py runserver 0.0.0.0:8000