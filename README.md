# Basic Python in Docker example
- The `Dockerfile` gives structure to the Docker image for this Python example.
- Running `docker build -t python-docker .` will build the image, so that it can be used locally by Docker.
- Once built, running `docker run python-docker` will execute the application.
- You can avoid writing an entire new Dockerfile for basic use cases, e.g.:
```
docker run -it --rm --name my-first-python-script -v "$PWD"/simple-example:/simple-example python:3 python /simple-example/simple-script.py
```
You could run this from the docroot of this project, and it will mount the `simple-example` folder to the container, and then execute Python from the root of the container, which at that point will have matched the folder structure of `simple-example/simple-script.py`.