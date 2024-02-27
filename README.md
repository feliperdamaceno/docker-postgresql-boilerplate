## Docker PostgreSQL Boilerplate

### 1. Database container setup:

First, go to the **docker-compose.yml** file and setup a password for the environment variables `POSTGRES_PASSWORD` and `PGADMIN_DEFAULT_PASSWORD`.

After doing that, run the following command to create your Postgres service:

```bash
docker compose -p postgres up -d
```

Note: To take down the docker services, just use:

```bash
docker-compose -p postgres down
```

### 2. pgAdmin setup:

Once your containers are up and running, navigate to http://localhost:8000 to access your pgAdmin service, then login with the email admin@superuser.com, and the password you setup in the `PGADMIN_DEFAULT_PASSWORD` variable on your **docker-compose.yml** file.

Next, create a new server connection and name your server as desired.

Finally, on the Connection tab, add the **Host name/address** as **postgres**, Username as **admin**, Port is **5432**, and the password as `POSTGRES_PASSWORD` setup on the **docker-compose.yml** file, then click save.

After doing that, pgAdmin should be connected to the Postgres database.

### 3. Environment variables setup:

Create a .env file with a variable called `POSTGRES_URL`, following the example below:

```bash
POSTGRES_URL=postgresql://username:password@localhost:port/database
```
