# 🍔 CigBurger Dockerized

This is my version of the CigBurger backoffice project built in the course "[2024] CodeIgniter 4 - 3 large PROFESSIONAL projects united by APIs | MVC | PHP8 | MySQL | All about one structure!" from Udemy. This project combines three smaller projects into one unified system using Docker. Each of the original projects is connected via API, and Docker is used to streamline the setup and management of these services.

## 📋 Prerequisites

Before setting up CigBurger Dockerized, ensure you have the following installed on your machine:

- 🐳 Docker: [Install Docker](https://docs.docker.com/get-docker/)
- 🐙 Docker Compose: [Install Docker Compose](https://docs.docker.com/compose/install/)

## 🚀 Setup

Follow these steps to set up and run the CigBurger Dockerized project:

1. **Clone the Repository**
   ```bash
   git clone https://github.com/joaotfrodrigues/cigburger_dockerized.git
   cd cigburger-dockerized
   ```

2. **Build and Start the Docker Containers**
   ```bash
   docker-compose up -d --build
   ```

3. **⏳ Wait for the Services to Start**
   The project may take 10-15 seconds to start as migrations and seeds are running in the Spark container.

4. **🌐 Access the Application**
   The services should now be running and accessible at the following URLs:
   - CigBackoffice: [http://localhost:8000](http://localhost:8000)
   - CigRequest: [http://localhost:8001](http://localhost:8001)
   - CigKitchen: [http://localhost:8002](http://localhost:8002)
   - phpMyAdmin: [http://localhost:8080](http://localhost:8080)

## 🔗 More Information

For more information on how the API works and details about the individual projects, visit the following GitHub repositories:

- CigBackoffice: [https://github.com/joaotfrodrigues/cigburger_backoffice](https://github.com/joaotfrodrigues/cigburger_backoffice)
- CigRequest: [https://github.com/joaotfrodrigues/cigburger_request](https://github.com/joaotfrodrigues/cigburger_request)
- CigKitchen: [https://github.com/joaotfrodrigues/cigburger_kitchen](https://github.com/joaotfrodrigues/cigburger_kitchen)
