# pyramid-hello

Hello world web application using the Pyramid web framework.

Based on https://docs.pylonsproject.org/projects/pyramid/en/latest/quick_tutorial/hello_world.html


## Usage

Build a Docker image with the pre-requisites:

```
docker build -t pyramid-hello .
```

Execute the application in a Docker container:

```
docker run \
  --rm \
  -it \
  -v $(pwd):$(pwd) \
  -w $(pwd) \
  --network=host \
  --user $(id -u $(whoami)):$(id -g $(whoami)) \
  pyramid-hello \
  python app.py
```

Open http://localhost:6543/ in your browser.`
