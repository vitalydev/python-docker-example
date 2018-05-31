# microservice

This is application example using Python, PostgreSQL, Docker.

# Running the environment

You need to have Docker installed in your machine, after that, just run commands:

Start services:

`docker swarm init`
`docker-compose build`

`docker service create --name registry --publish published=5000,target=5000 registry:2`
`docker-compose push`

`docker stack deploy --compose-file docker-compose.yml python-docker-example`

Run migrations:

1. Run `docker ps`
2. Choose container
3. Run `docker exec -t -i 5dbeb6304c00 bash`
Replace 5dbeb6304c00 with web container ID.
4. Run `./manage.py migrate`

Stop services:

`docker stack rm python-docker-example`
`docker service rm registry`
`docker swarm leave --force`

Check status:

`docker stack services python-docker-example`

Go to: http://localhost:8000/books/