# spring-boot-app
playing with the spring boot and postgres

# DB
* Spawn a postgres DB in a docker container

`docker run --name demodb -e POSTGRES_PASSWORD=password -d -p 5432:5432 postgres:alpine`

* Create database

`docker exec -it 7b62419c80be bin/bash`

`bash-5.0# psql -U postgres`

`postgres=# CREATE DATABASE demodb;`

`postgres=# \c demodb`

* Insert some data

`demodb=# CREATE EXTENSION "uuid-ossp";`

`demodb=# INSERT INTO person (id, name) VALUES (uuid_generate_v4(), 'Svilen Velikov');`
