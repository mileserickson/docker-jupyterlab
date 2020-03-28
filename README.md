# docker-jupyterlab

A quick experiment to create a self-contained repo for JupyterLab in a container, with a mapped directory for notebooks.

Use at your own risk.

## Prerequisites

* Docker

## Instructions

Steps to success:

### 1. Open a Terminal.

On a Linux or Mac computer, this will be your normal Terminal application. If you're on a Windows machine, please use Git Bash (not Command Prompt or PowerShell).

### 2. Fork and clone the repository.

`git clone git@github.com:your_username/docker-jupyterlab`

(Note: If you have have not yet GitHub configured to use SSH, replace `git@github.com:` with `https://github.com/`.)

### 3. Change into this repository's directory.

`cd docker-jupyterlab`

### 4. Build the container

To build the container from the Dockerfile:
`docker build -t jupyterlab .` 
(Note: your first build requires large downloads and may be time-consuming.)

### 5. Run JupyterLab in the container

`docker run -v 48080:48080 -p $(pwd)/nb:/nb jupyterlab`

### 6. Access JupyterLab in the broswer

The terminal will display a URL referencing `localhost` or `127.0.0.1`. Paste that URL into a web browser.
