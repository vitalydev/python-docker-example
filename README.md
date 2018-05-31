# microservice

This is application example using Python, PostgreSQL, Docker.

# Running the environment

You need to have Docker installed in your machine, after that, just run commands:

`docker-compose build`

`docker-compose run web ./manage.py migrate`

`docker swarm init`

`docker-compose up`

Go to: http://localhost:8000/books/