# Smatech Store Deployment

This repository contains the necessary deployment files for Smatech Store. These files automate the process of deploying the store to a server using Docker.

## Prerequisites
Ensure the target machine has Docker installed and running before proceeding with the deployment.

## Deployment Steps

### 1. Create a Docker Network
To enable communication between services, create a Docker network named `smatech`:
```bash
docker network create smatech
```

### 2. Set Permissions for Initialization Script
The database initialization script (`init-db.sh`) requires execution permissions:
```bash
chmod +x init-db.sh
```
**Note for Windows Users:** Use **WSL** to run the above command instead of Command Prompt or PowerShell.

### 3. Start the Deployment
Run the following command to deploy the store:
```bash
docker-compose up -d
```

### 4. Stop the Deployment
To stop the store services, run:
```bash
docker-compose down
```

## Accessing the Store
Once the deployment is complete, you can access the store using:
```bash
http://localhost
```
Ensure that **port 80 is available** on the server before deployment.

## Admin Dashboard Credentials
Use the following credentials to log in to the admin dashboard:
```bash
Username: admin@hardcoded.com
Password: Password123#
```

To Access the Admin Dashboard click on the admin link at the top ,from there you can create and manage products, categories, view orders, manage orders, and view admins

## Services Used
The Smatech Store system consists of the following microservices:
- **Eureka Server** – Service Discovery (https://github.com/asheckn/smatech-service-registry)
- **API Gateway** – Routing & Security (https://github.com/asheckn/smatech-api-gateway)
- **Authentication Service** – User Management (https://github.com/asheckn/smatech-authentication-service)
- **Store Service** – Product Management (https://github.com/asheckn/smatech-store-service)
- **Payment Service** – Payment Processing (https://github.com/asheckn/smatech-payment-service)
- **PostgreSQL Service** – Database
- **Angular Frontend Service** – User Interface  (https://github.com/asheckn/smatech-front)


## Test Payment Credentials
For testing payments, use the following credentials:
```bash
Username: sb-or43c4736845103@personal.example.com
Password: FUx9[g<<
```

## Notes
- Make sure all required ports are available on the server before deployment.
- The application requires the `smatech` network for inter-service communication.
- Ensure that Docker is properly installed and running before starting the deployment.

---
This guide ensures a smooth deployment process for Smatech Store. If you encounter any issues, verify that all services are running and configured correctly.

