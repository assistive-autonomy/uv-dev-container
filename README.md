# uv-dev-container

[![Docker Image CI](https://github.com/assistive-autonomy/uv-dev-container/actions/workflows/docker-ci.yml/badge.svg)](https://github.com/assistive-autonomy/uv-dev-container/actions/workflows/docker-ci.yml)

A no-nonsense CUDA-enabled dev container with **uv**, GPU support, and essential tooling. Built for AI/ML projects and remote development. Automatically published to GitHub Container Registry on every push to `main`.

## Quick Start

Pull and run the latest image:

```bash
docker pull ghcr.io/assistive-autonomy/uv-dev-container:latest
docker run -it ghcr.io/assistive-autonomy/uv-dev-container:latest bash

# With GPU support
docker run --gpus all -it ghcr.io/assistive-autonomy/uv-dev-container:latest bash
```

## Available Tags

- `latest` - Current stable build
- `X.Y.Z` - Version-specific tags (pulled from `pyproject.toml`)

Full registry: https://github.com/assistive-autonomy/uv-dev-container/pkgs/container/uv-dev-container

## What's Inside

- **CUDA 12.0** for GPU acceleration
- **uv** - blazingly fast Python package manager
- **VS Code CLI** for remote development
- **Dev tools**: git, git-lfs, gcc, tmux, curl, wget, vim
- Built on Ubuntu 22.04

## How It Works

GitHub Actions automatically:
1. Builds the Docker image on every push to `main`
2. Extracts the version from `pyproject.toml`
3. Tags with both version number and `latest`
4. Pushes to `ghcr.io`
