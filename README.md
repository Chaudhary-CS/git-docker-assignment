# Git and Docker Starter Application

This repository contains a small Python web application used to practice Git, GitHub, and Docker workflows.

## Application

The app runs in a Docker container, listens on port 8000, and returns its name and a health status line.

## Verification

The running application should be verified using an HTTP request to port 8000.

## Usage

Build the image:

    docker build -t git-docker-app:test .

Run it:

    docker run -d --name app-test -p 8080:8000 git-docker-app:test

Then check it's working:

    curl http://localhost:8080

When you're done:

    docker stop app-test
    docker rm app-test
