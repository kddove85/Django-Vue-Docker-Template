FROM  python:3.11

ENV PYTHONUNBUFFERED=1

WORKDIR /usr/src/app

RUN pip install django django-cors-headers python-decouple gunicorn uvicorn

COPY . .

EXPOSE 8000

ENTRYPOINT ["/usr/src/app/docker-entrypoint.sh"]

CMD ["sh", "-c", "gunicorn sample_project.asgi:application -k sample_project.uvicorn.GunicornUvicornWorker"]