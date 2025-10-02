# build image
docker build -t flask-hello .

# run container
docker run -p 3000:3000 flask-hello
