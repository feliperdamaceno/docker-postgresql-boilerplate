## Docker PostgreSQL Boilerplate

### 1. Postgres Setup:

Use `.env.example` file as a reference to setup the required environment variables.

After doing that, run the following command to create your Postgres service:

```bash
docker compose -p postgres up -d
```

To take down the docker services, just use:

```bash
docker-compose -p postgres down
```

### 2. pgAdmin Setup:

Once your containers are up and running, navigate to http://localhost:8080 to access your pgAdmin service, then login with the credentials set in your `.env` file.

Next, create a new server connection and name your server as desired.

Finally, in the Connection tab, set **Host name/address** as **postgres**, **Username** and **Password** as set in your `.env` file, and **Port** number as **5432**, then click save.

Once done, pgAdmin should be connected to the Postgres database.

When consuming your Postgres database, use the following URL structure:

```
postgresql://USERNAME:PASSWORD@localhost:PORT/DATABASE_NAME
```
