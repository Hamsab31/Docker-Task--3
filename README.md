Custom Nginx Docker
A simple project to create a custom Nginx Docker image, deploy it using Docker Compose, and serve a custom index.html from a bind-mounted volume (/var/opt/nginx).
Files
Dockerfile – Builds the custom Nginx image
docker-compose.yaml – Service & volume setup
index.html – Sample web page
nginx.conf – Nginx configuration
Setup & Run
# Clone the repo
git clone https://github.com/YOUR-USERNAME/nginx-docker-project.git
cd nginx-docker-project

# Build and run
docker-compose build
docker-compose up -d
Open your browser at: http://<EC2-PUBLIC-IP>
Push Image to Docker Hub
docker login
docker tag h4meed/nginx-custom:latest h4meed/nginx-custom:latest
docker push h4meed/nginx-custom:latest
Notes
The HTML file is mounted at /var/opt/nginx in the container.
Nginx serves content from the bind-mounted volume.
Container restarts automatically if stopped (restart: unless-stopped).
