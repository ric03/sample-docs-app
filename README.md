# Simple Docs App

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
