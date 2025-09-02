# Ory Kratos Custom Setup

This project provides a **custom setup of [Ory Kratos](https://www.ory.sh/kratos/)**.  
It includes a Dockerfile that copies and applies a custom `kratos` configuration, making it easier for users to run and extend Kratos in their environment.  

---

## 🚀 Features
- Custom **Kratos configuration** baked into the Docker image.  
- Build and publish Docker images with [Proto](https://moonrepo.dev/proto).  
- Run locally with **Docker**.  
- Supports environment configuration via `.env`.  

---

## 🛠️ How to Run  

### 1. Install prerequisites
Make sure you have the following installed:  
- [Docker](https://docs.docker.com/get-docker/)  
- [Proto](https://moonrepo.dev/proto)  

---

### 2. Environment variables
First, create a `.env` file by copying the sample and updating it with your own values:  

```bash
cp env.sample .env
```

Modify the values in `.env` according to your setup (database, registry, secrets, etc.).  

---

### 3. First-time setup
Run the following command to initialize proto and install dependencies:

```bash
proto use
```

---

### 4. Build the Docker image
Build the image locally using Proto:

```bash
moon :docker
```

---

### 5. Publish to container registry
Push the image to your preferred registry:

```bash
moon :publish
```

---

### 6. Run the services
Start everything with Docker:

```bash
docker compose up -d

---

### 2. Environment variables
First, create a `.env` file by copying the sample and updating it with your own values:  

```bash
cp env.sample .env
