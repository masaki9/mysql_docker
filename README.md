# MySQL 8 Docker Setup

This repository provides a simple way to run MySQL 8 using Docker. It includes SQL data files that are automatically loaded into MySQL upon initialization for testing purposes. The container is configured to allow the root user to log into MySQL without a password.

## Getting Started

Follow these steps to get your MySQL container up and running:

### 1. Clone the Repository
```bash
git clone https://github.com/masaki9/mysql_docker.git
cd mysql_docker
```

### 2. Start the MySQL Container

```bash
docker compose up -d
```

### 3. Connect to MySQL
```bash
mysql -h 127.0.0.1 -P 3306 -u root
```

**Note:** You can also connect using a MySQL client like MySQL Workbench by entering the following details:
- **Hostname:** `127.0.0.1`
- **Port:** `3306`
- **Username:** `root`
- **Password:** (leave blank)

### 4. Stopping the Container
```bash
docker compose down
```

## Included SQL Files

The `data` directory contains several SQL and dump files that are automatically executed when the MySQL container is started for the first time. These files set up a few databases and load sample data:

- `01-sakila-schema.sql`: Schema for the Sakila sample database.
- `02-sakila-data.sql`: Data for the Sakila sample database.
- `employees.sql`: Schema and data for the Employees sample database.
- `Dump files`: Include files like `load_departments.dump`, `load_employees.dump`, etc., which load additional data into the Employees database.
- `world.sql`: Schema and data for the World sample database.
