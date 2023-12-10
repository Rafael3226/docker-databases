# Set up PostgreSQL & pgAdmin with Docker

This guide will help you set up a PostgreSQL database along with the pgAdmin4 web-based database management tool using Docker containers.

[TOC]

## Setup

### Prerequisites

Before you begin, make sure you have the following software installed:

- Docker: Check if Docker is installed by running the following commands:

  ```bash
  docker -v
  ```

- Docker Compose: Check if Docker Compose is installed:

  ```bash
  docker-compose -v
  ```

### Start Docker Compose

To start the PostgreSQL and pgAdmin4 containers, use the following command:

```bash
docker-compose up
```

This command will download the necessary Docker images (if not already downloaded) and launch the containers.

### Stopping Containers

To stop the running containers (PostgreSQL and pgAdmin4), use the following command:

```bash
docker-compose down
```

This will stop the containers but retain the database data.

### Delete Database (Including Data)

If you want to completely remove the PostgreSQL database along with its data, use the following command:

```bash
docker-compose down -v
```

This command will stop the containers and also delete the database data. Be cautious when using this command, as it will irreversibly delete data stored in volumes.

## Usage

### Connect to the Database

You can connect to the PostgreSQL database using your preferred database client, specifying the following credentials:

- Host: `10.0.0.2` or the IP address of your machine.
- Port: `5432`
- Username: `postgres` (or your specified username)
- Password: `postgres` (or your specified password)
- Database Name: `postgres` (or your specified database name)

### Access pgAdmin4

pgAdmin4 is a web-based database management tool that you can access in your web browser. To access pgAdmin4:

- Open your web browser.
- Navigate to `http://localhost:5050`.

You can log in to pgAdmin4 with the following credentials:

- Email/Username: `admin@email.com`
- Password: `admin`

Once logged in, you can set up connections to your PostgreSQL database and manage it through the pgAdmin4 interface.

Enjoy using PostgreSQL and pgAdmin4 with Docker for your database needs!
