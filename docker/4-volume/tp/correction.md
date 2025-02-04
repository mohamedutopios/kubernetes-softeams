# Create the volume
docker volume create shared_data

# Run the writer container
docker run --name writer-container -v shared_data:/shared_data -d alpine sh -c 'while true; do echo "Current time: $(date)" > /shared_data/index.html; sleep 1; done'

# Run the Nginx container
docker run --name nginx-container -v shared_data:/usr/share/nginx/html:ro -d -p 8080:80 nginx

# Check the output
curl http://localhost:8080
