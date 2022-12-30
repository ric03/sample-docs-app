# Simple Docs App

This is the application repo for the [sample-docs-deployment](https://github.com/ric03/sample-docs-deployment).

This app uses [Material for MkDocs](https://squidfunk.github.io/mkdocs-material)

# Build the app

```shell
python -m pip install mkdocs-material
python -m pip mkdocs build
```

This will generate `site` folder containing the static html files.

# Build the image

Build an image based on nginx, with the default config.

```shell
docker build . -t <tag>
```

Run the image locally

```shell
docker run <tag> -p 8081:80 --name localnginx -d
```

# GH Actions Workflow

The GH Action generates the static files, packages them as a nginx image and pushes the image to the GitHub Container
Registry (https://ghcr.io)
