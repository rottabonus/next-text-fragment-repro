
# build image
docker build -t astro-hello .

# run container
docker run -p 3000:3000 astro-hello
