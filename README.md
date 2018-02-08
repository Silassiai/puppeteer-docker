# pluswerk/puppeteer
Opinionated puppeteer Headless Chrome

example docker-compose.yml
````yaml
version: '3'

services:
  puppeteer:
    image: pluswerk/puppeteer
    volumes:
      - ./:/app/
    working_dir: /app/
    shm_size: 1gb
    # just run the container doing nothing
    entrypoint: ["sh", "-c", "sleep infinity"]
````

Then use ``docker-compose exec puppeteer`` to execute your node script in the container.
