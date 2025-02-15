# smatech-deploy
Smatech store deployment repository 

This repository contains the deployment files for the Smatech store. The deployment files are used to deploy the store to the server.
To get setup make sure the target machine has Docker installed and its running 

To deploy the store to the server, follow the steps below:
create a network on docker called smatech
```bash

docker network create smatech
```

You need to give the file ini-db.sh the correct permissions
```bash

chmod +x init-db.sh

```

for windows use wsl for the same commands not terminal or powershell



Then run the following command to deploy the store to the server
```bash
docker-compose up -d
```
To stop the store from running on the server, run the following command
```bash
docker-compose down
```
When the store is running use the following credentials to login to the admin dashboard
```bash
username: admin@hardcoded.com
password: Password123#
```

To access the store, use the following URL
```bash
http://localhost
```
Make sure port 80 is available on the server before deploying the store

The services the system use are 
Eureka Server
Api Gateway
Authentication Service
Store Service
Payment Service 
PostgresSQL Service
Angular Frontend Service