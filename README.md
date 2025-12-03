# Build it (the dot means "current folder")
docker build -t myapp .

# Run it
docker run -td -p 5000:5000 myapp

# Test it
curl localhost:5000
# Or open browser: http://localhost:5000


# Login to Docker Hub (create free account first at hub.docker.com)
docker login

# Tag your image with your username
docker tag myapp yourusername/myapp:1.0

# Push it
docker push yourusername/myapp:1.0

# Now delete local copy
docker rmi yourusername/myapp:1.0

# Pull and run from Docker Hub
docker run -td -p 5000:5000 yourusername/myapp:1.0
# It downloads and runs!
