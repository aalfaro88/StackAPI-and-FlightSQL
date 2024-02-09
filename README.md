# FullStack Challenge 
Flask | React | MYSQL | Docker

## Overview

This project is a full-stack application designed to showcase a technical challenge for a FullStack MD role. The application integrates a React-based frontend, a Flask backend, and a MySQL database, all containerized using Docker. The backend fetches data from the Stack Exchange API and also serves data from a MySQL database regarding airline and airport operations. The frontend displays this data in an informative and user-friendly manner.

## Features

- **React Frontend:** Displays data fetched from the backend in a clear and interactive format, including information from the Stack Exchange API and SQL queries related to airline operations.
- **Flask Backend:** Serves data from the Stack Exchange API and a MySQL database through RESTful endpoints.
- **MySQL Database:** Stores and manages data regarding airlines, airports, and their operations.
- **Dockerized Application:** Ensures easy setup and deployment by containerizing the frontend, backend, and database.

## Prerequisites

Before you begin, ensure you have Docker installed on your system. If not, you can download and install Docker from [Docker's official website](https://www.docker.com/products/docker-desktop).

## Setup and Running the Application

1. **Clone the Repository**

   Begin by cloning the repository to your local machine:

```bash
    git clone https://github.com/aalfaro88/StackAPI-and-FlightSQL
    cd StackAPI-and-FlightSQL
```

2. **Setting Up Environment Variables**

Before running your application, you need to configure the database connection details. To do this, go to the .env file found backend folder and adjust the following lines with your own credentials:

```bash
# Database Configuration of MYSQL
DB_USERNAME=root  # IMPORTANT: The username for your database; change if not using the default root user
DB_PASSWORD=ironhack  # IMPORTANT: The password for your database user 
DB_NAME=airplane_database  # The name of your database, no need to modify it.
DB_PORT=3306  # The port your database server is listening on, typically 3306 for MySQL.
```

If you are unfamiliar with MySQL, do not have it installed, or need to set up your database credentials, consult the [MySQL Getting Started Documentation](https://dev.mysql.com/doc/mysql-getting-started/en/). This guide provides detailed instructions on installing MySQL, setting up your initial user, and creating a database.

3. **Build the Docker Containers and Run**

Use Docker Compose to build the application containers. This command builds the backend, frontend, and database containers according to the specifications in the docker-compose.yml file:

```bash
git docker-compose up --build
```

4 **Accessing the Application**

Once the containers are running, you can access the frontend application by navigating to http://localhost:3000 in your web browser. The backend API will be available at http://localhost:5001.

## Stopping the Application

To stop the running containers, you can use the following command:

```bash
docker-compose down
```
This command stops and removes the containers, networks, and volumes created by docker-compose up.

## Additional Notes ##

- The MySQL database is initialized with predefined data for airlines, airports, and flights. You can interact with this data through the backend API endpoints.
- The frontend is designed to consume the backend endpoints and display the data in an interactive format.



