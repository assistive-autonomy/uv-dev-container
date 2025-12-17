# uv-dev-container

[![Docker Image CI](https://github.com/assistive-autonomy/uv-dev-container/actions/workflows/docker-ci.yml/badge.svg)](https://github.com/assistive-autonomy/uv-dev-container/actions/workflows/docker-ci.yml)

## Quick Start

Pull and run the latest image:

```bash
docker pull assistiveautonomy/uv-dev-container:latest
docker run -it assistiveautonomy/uv-dev-container:latest bash

# With GPU support
docker run --gpus all -it assistiveautonomy/uv-dev-container:latest bash
```

## What's Inside

- **CUDA 12.0** for GPU acceleration
- **uv** - blazingly fast Python package manager
- **VS Code CLI** for remote development
- **Dev tools**: git, git-lfs, gcc, tmux, curl, wget, vim, 
- Built on Ubuntu 22.04
