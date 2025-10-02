
# build image
docker build -t nextjs-hello .

# run container
docker run -p 3000:3000 nextjs-hello
