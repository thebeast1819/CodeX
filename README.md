
# CODEX

CODEX is a Remote Code Executor which lets you execute short code snippets of yours remotely.


## Features

- Implemented Code Santization
- For each code run request, a seperate Docker container is created which limits the interference with the host machine.
- Socket has been implemented with rooms, allowing multiple users to come together and code along in different rooms.
- The parameters like Time taken to run the code and Total memory used have been limited, allowing efficient management of resources.
- The code execution happens asynchronously, allowing the server to handle multiple requests at the same time.


## Tech Stack

**Client:** React

**Server:** Node, Express, Docker


## Prerequisites

- docker

```bash
    curl -fsSL https://get.docker.com -o get-docker.sh
```

```bash
    sudo sh get-docker.sh
```

## Run Locally

Clone the project

```bash
  git clone https://github.com/thebeast1819/CodeX
```

Go to the backend project directory

```bash
  cd remote-code-executor/backend
```

Install dependencies

```bash
  npm install
```

Build the Docker images

```bash
  cd Dockerfiles
```

```bash
  sudo docker build -t java:v1 ./java 
```
```bash
  sudo docker build -t cpp:v1 ./cpp 
```
```bash
  sudo docker build -t py:v1 ./python 
```

## Usage

- To start the backend server in Development mode

```bash
cd backend && npm run dev
```

- To start the backend server in Production mode

```bash
cd backend && npm run start
```

- Start the frontend server

```bash
cd ../frontend && npm start
```
