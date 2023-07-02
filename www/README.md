# PHP REST API

This is a simple REST API written in PHP without any dependencies or frameworks.

Data is stored in a MySQL database and can be browsed using a very simple Angular webapp. 

The API and database is run as a Docker container using Docker Compose. 

### Components

- Backend: [PHP][php], [MySQL][mysql]
- Frontend: [Angular][angular]

# Prerequisites&nbsp;:vertical_traffic_light:
- [Git][git:download]
- [PHP][php:download]
- [Docker][docker:download]

# Getting started&nbsp;:runner:

### Getting the code&nbsp;:octocat:

- Clone the repository: `git clone https://github.com/taardal/php-rest-api`

### Running the app&nbsp;:rocket:

**Backend**

- Make sure Docker is running
- Navigate to the server: `cd api`
- Run the Docker container: `docker-compose up`

**Frontend**

- Navigate to the client: `cd www`
- Run the Angular webapp: `npm start`

# Docker&nbsp;:whale:

The REST API is run as a Docker container using Docker Compose. 

- `./api/docker-compose.yml`
- `./api/docker/mysql/Dockerfile`
- `./api/docker/php-apache/Dockerfile`

**MySQL**

Sample data is added to the database using the bundled `schema.sql` file

- `./api/docker/mysql/docker-entrypoint-initdb.d/schema.sql`

**Apache**

Apache is configured using the bundled `httpd.conf` file

- `./api/docker/php-apache/httpd.conf`


[angular]: https://angular.io/
[docker:download]: https://www.docker.com/get-started/
[git:download]: https://git-scm.com/downloads
[mysql]: https://www.mysql.com/
[php]: https://www.php.net/
[php:download]: https://www.php.net/downloads.php

