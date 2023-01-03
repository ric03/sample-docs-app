# Simple Docs App

This is the application repo for the [sample-docs-deployment](https://github.com/ric03/sample-docs-deployment).

This repo is part of an ArgoCD experiment, see https://github.com/ric03/sample-docs-argocd

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://github.com/ric03/sample-docs-argocd/raw/main/docs/component-overview-transparent-darkmode.png">
  <img alt="Component Overview" src="https://github.com/ric03/sample-docs-argocd/raw/main/docs/component-overview-transparent.png">
</picture>

# Build the app

This app uses [Material for MkDocs](https://squidfunk.github.io/mkdocs-material)

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
