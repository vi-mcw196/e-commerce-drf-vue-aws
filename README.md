# E-Commerce Platform with Monolith Architecture

## Table of Contents

- [E-Commerce Platform with Monolith Architecture](#e-commerce-platform-with-monolith-architecture)
  - [Table of Contents](#table-of-contents)
  - [Overview](#overview)
  - [Key Features](#key-features)
    - [1. **User Management**](#1-user-management)
    - [2. **Product Management**](#2-product-management)
    - [3. **Basket Management**](#3-basket-management)
    - [4. **Order Processing**](#4-order-processing)
    - [5. **Recommendation Engine**](#5-recommendation-engine)
  - [Technology Stack](#technology-stack)
    - [**Backend**](#backend)
    - [**Frontend**](#frontend)
    - [**Database**](#database)
  - [Infrastructure and Deployment](#infrastructure-and-deployment)
    - [**AWS Services**](#aws-services)
    - [**Terraform and Ansible**](#terraform-and-ansible)
    - [**Docker and Docker Compose**](#docker-and-docker-compose)
  - [Security](#security)
  - [Advanced Features](#advanced-features)
    - [**AI/ML Integration**](#aiml-integration)
    - [**Performance Optimization**](#performance-optimization)
    - [**CI/CD Pipelines**](#cicd-pipelines)
  - [How to Run the Project](#how-to-run-the-project)
    - [Prerequisites](#prerequisites)
    - [Steps to Deploy](#steps-to-deploy)
  - [Future Enhancements](#future-enhancements)
  - [Author](#author)

---

## Overview

This project is a monolithic e-commerce platform designed to provide users with a seamless shopping experience. The platform integrates user account management, product browsing, basket management, order processing, and a recommendation engine into a single application. Built as a monolithic architecture, it handles all components under one unified system.

> [!NOTE] 
>
> - All project documentation can be found under the `design` folder.  
> - The README files for this project are located in the `design` folder.  

[🔝 Back to Table of Contents](#table-of-contents)

---

## Key Features

### 1. **User Management**

- User registration and login.
- Profile management and account updates.

[🔝 Back to Table of Contents](#table-of-contents)

### 2. **Product Management**

- Administrators can add, edit, and delete products in the catalogue.
- Dynamic product browsing for users.

[🔝 Back to Table of Contents](#table-of-contents)

### 3. **Basket Management**

- Add products to the basket.
- Adjust quantities and remove items.
- Proceed to checkout with a streamlined interface.

[🔝 Back to Table of Contents](#table-of-contents)

### 4. **Order Processing**

- Complete purchase workflow, including:
  - Payment processing.
  - Order confirmation.
  - Tracking order status.

[🔝 Back to Table of Contents](#table-of-contents)

### 5. **Recommendation Engine**

- Personalized product suggestions based on:
  - User behavior.
  - Browsing history.
  - Previous purchases.

[🔝 Back to Table of Contents](#table-of-contents)

---

## Technology Stack

### **Backend**

- **Django**: Provides the core server-side logic.
- **Django REST Framework**: API development for backend and frontend communication.

[🔝 Back to Table of Contents](#table-of-contents)

### **Frontend**

- **React**: User-friendly interface for seamless interactions.

[🔝 Back to Table of Contents](#table-of-contents)

### **Database**

- **AWS RDS (PostgreSQL/MySQL)**: Handles relational data like users, orders, and products.

[🔝 Back to Table of Contents](#table-of-contents)

---

## Infrastructure and Deployment

### **AWS Services**

1. **EC2**: Hosts the monolithic backend application.
2. **Elastic Beanstalk**: Simplifies deployment with automatic scaling and load balancing.
3. **S3**: Stores media assets such as product images.
4. **Amazon SES/SNS**: Sends email notifications for order confirmations and other events.
5. **CloudWatch**: Monitors application performance and logs.
6. **Elastic Load Balancer**: Manages traffic spikes by balancing load across servers.
7. **CloudTrail**: Tracks API activity and user actions for auditing.
8. **AWS Lambda**: Executes tasks like real-time notifications or asynchronous data processing.

[🔝 Back to Table of Contents](#table-of-contents)

---

### **Terraform and Ansible**

- **Terraform**: Automates the provisioning of cloud infrastructure, including EC2 instances, S3 buckets, and RDS databases.  
- **Ansible**: Handles configuration management, ensuring all servers are consistently set up for application deployment.

> [!NOTE] 
> The entire infrastructure is deployed using **Terraform** and configured with **Ansible** for efficiency and consistency.

[🔝 Back to Table of Contents](#table-of-contents)

---

### **Docker and Docker Compose**

- **Docker**: Containerizes the application, ensuring consistency between development and production environments.  
- **Docker Compose**: Orchestrates multi-container deployments for local development, making it easy to run the full application stack.

> [!IMPORTANT]  
> Local development requirements, including the database and frontend/backend services, are fully managed using **Dockerfiles** and **Docker Compose**.

[🔝 Back to Table of Contents](#table-of-contents)

---

## Security

1. **Amazon Cognito**: Manages user authentication and authorization.
2. **AWS IAM**: Ensures secure access to AWS resources.
3. **AWS Secrets Manager**: Handles sensitive credentials (e.g., API keys, database credentials) securely.

[🔝 Back to Table of Contents](#table-of-contents)

---

## Advanced Features

### **AI/ML Integration**

- **Amazon SageMaker**: Builds a recommendation system to provide personalized suggestions.

[🔝 Back to Table of Contents](#table-of-contents)

### **Performance Optimization**

- **AWS ElastiCache (Redis/Memcached)**: Improves response times by caching frequently accessed data.

[🔝 Back to Table of Contents](#table-of-contents)

### **CI/CD Pipelines**

- **AWS CodePipeline**: Automates deployment for faster and more reliable updates.

[🔝 Back to Table of Contents](#table-of-contents)

---

## How to Run the Project

### Prerequisites

- AWS account with necessary permissions.
- Installed dependencies: Terraform, Ansible, Docker, Django, React.
- Configured access to AWS services (EC2, RDS, S3, etc.).

[🔝 Back to Table of Contents](#table-of-contents)

### Steps to Deploy

1. **Clone the Repository**

   ```bash
   git clone https://github.com/your-repo/ecommerce-platform.git
   cd ecommerce-platform
   ```

2. **Infrastructure Setup**
   - Initialize and deploy the infrastructure with Terraform:

     ```bash
     terraform init
     terraform apply
     ```

   - Configure the environment using Ansible:

     ```bash
     ansible-playbook -i inventory playbook.yml
     ```

3. **Local Development Setup**
   - Use Docker Compose to start services locally:

     ```bash
     docker-compose up
     ```

4. **Backend Setup**
   - Apply database migrations:

     ```bash
     python manage.py migrate
     ```

   - Start the backend server:

     ```bash
     python manage.py runserver
     ```

5. **Frontend Setup**
   - Navigate to the `frontend` directory.
   - Install dependencies and start the development server:

     ```bash
     npm install
     npm start
     ```

[🔝 Back to Table of Contents](#table-of-contents)

---

## Future Enhancements

- Add support for multi-language and multi-currency features.
- Introduce a microservices architecture for better scalability.
- Integrate additional analytics tools to track user behavior and improve the recommendation engine.

[🔝 Back to Table of Contents](#table-of-contents)

---

## Author

**Viktor Moldovan**  
**ID: 260311**  

Feel free to contribute or raise issues on GitHub to improve this project!  
