# Spot in

## Introduction

SpotIn is a place for registering spots. Spots can take place in the virtual or in the physical world. They capture the context and the circumstances that form the setting for an event. Each spot receives a stable Uniform Resource Identifier (URI) that can be used for referencing purposes. Spots can contain arbitrary metadata describing a context and circumstances. Additionally, spots can redirect the user to the original source of information. Once created, spots are searchable by places and by keywords.

## Prerequisites

The following prerequisites must be filled to run this service:

[Docker](https://docs.docker.com/get-docker/) must be installed. If you're on Windows, follow [this tutorial](https://docs.beescreens.ch/tutorials/install-and-configure-docker/)

[Visual Studio Code](https://code.visualstudio.com/download) must be installed

[Dev Container Extension](https://marketplace.visualstudio.com/items?itemName=ms-vscode-remote.remote-containers) must be installed

Open the repository in the dev Container, for more details, follow [this tutorial](https://docs.beescreens.ch/tutorials/install-and-configure-dev-containers/)

## Installation for local development

Open this folder in Visual Studio Code, and open it in a dev contianer

```bash
npm install

cp .env.defaults .env

# change DATABASE_SERVICE value to localhost in .env
# change SPOT_IN_BACKEND_URL value to localhost:3000 in .env

docker-compose up -d database

# watch mode
npm run dev
```

And the app is running on <http://localhost:3000>.

## Access the documentation

The API documentation is on <http://localhost:3000/api>.

## Running the app

```bash
# development
npm run start

# watch mode
npm run dev

# production mode
npm run start:prod
```

## Run the application for production

```bash
cp .env.defaults .env
# Change variable in .env for your configuration

docker compose build

docker compose up
```
