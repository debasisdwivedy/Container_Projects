# Build the image

docker build --rm -t python:alpine -f Python/Python .
docker build --rm -t java:alpine -f Java/Java .

# Run the conatiner

docker run -d --rm --name python -it python:alpine
docker run -d --rm --name java java:alpine

# Get the output

docker cp java:/usr/local/src/output.log .

# Stop the container

docker stop java
docker stop python

