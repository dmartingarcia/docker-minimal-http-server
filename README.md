# docker-homeautomation

It is part of a [set of repositories](https://github.com/search?q=user%3Admartingarcia+docker) that contain dockerised environments for small applications.

In this case, it contains a self-efficient minimal *http server* setup, that can serve static pages with a minimal memory footprint.

## How to use it

```
cp .env.example .env
docker-compose up -d
```

And browse into `http://localhost:9090`.

After that, you can also set your own files inside of the `/static` folder

## Traefik integration`

It also contains a Traefik integration, that interact with this reverse proxy, routing request to each container in case it matches the specified domain

There's a subdomain exposed:
  - apps.domain.com

## .env setup

It contains a basic set of variables like:

- http host that uses Traefik to match requests

## Docker Traefik

If you want to use this Traefik integration, [take a look at this repository](https://github.com/dmartingarcia/docker-traefik)
