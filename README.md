# Docker Static Site Tutorial

This repository contains a simple setup using Docker and Docker Compose to serve static HTML, CSS, and a blank JavaScript file with an Nginx server.

The HTML includes a boilerplate form and a section that prints the URL query parameters and uses Bootstrap for styling.

## Directory Structure

learning-web/
├── docker-compose.yml
├── Dockerfile
├── nginx.conf
└── static/
    ├── index.html
    ├── style.css
    └── script.js

## Prerequisites

You must install Git as well as Docker on your machine. Your Git tool must be associated with your GitHub account.

### Git and GitHub
The easiest way to install Git and have it tied to your GitHub account is to use the [GitHub Desktop app](https://desktop.github.com).

The more "advanced" way is to download Git from the [official downloads page](https://git-scm.com/downloads). From there you can clone your repository using HTTPS or SSH.

_Note:_ If you're using macOS or Linux and prefer to use the Git cli, make sure to also download the [Git Credential Manager](https://github.com/git-ecosystem/git-credential-manager). This will allow you to have your passwords saved when cloning repos using HTTPS.

### Docker and Docker Compose

To install Docker and Docker Compose simply visit the official [Docker website](https://docs.docker.com/engine/install/)

## Setup Instructions

### Step 0: Fork the repository

Make sure you fork this repository first so that you can continue to the next step. You do this by logging in to your GitHub account, and click on the Fork button on this repository.

### Step 1: Clone the Repository

We have two options to clone the repository. One option is to use the GitHub Desktop Application and the other option is to clone using the `git` command line interface.

Additionally, using the `git` command line interface offers two ways of cloning: using HTTPS and using SSH.

GitHub is recommending cloning repositories using HTTPS, and if it's your first time using the `git` command line interface then follow their guide here.

If you want to clone GitHub repositories using SSH you can still do so by following the steps in the following guide.

Once you've forked the repository through the GitHub web UI and authenticated / tied your machine's `git` with GitHub you are now ready to clone the repository.

#### Cloning with the `git` command line interface

Navigate to an appropriate directory - like `My Documents` in Windows or `Documents` in a Unix machine - in your terminal and run the following command:

```bash
# To clone using https:
git clone https://github.com/<your-username>/learning-web.git

# To clone using ssh:
git clone git@github.com:<your-username>/learning-web.git

# change directory to the newly cloned repository
cd learning-web
```

#### Cloning with the `GitHub Desktop` application

If you don't want to use the command line then you can clone the repository through the GitHub Desktop App and follow the prompts.

### Step 2: Run and build the container

In your terminal, navigate to the project's root directory and run

```bash
docker-compose up -d
```

This command is a shorthand for the following two commands `docker-compose build` and `docker-compose up` in detached mode.

### Step 3: Verifying that everything worked

Open a new web browser and visit: `http://localhost:8080`. You should be presented with the sample index page.

### Step 4: Stopping the container

To stop your container, in your terminal navigate to the project's root directory and run

```bash
docker-compose down
```
