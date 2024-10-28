# CRUD Web Server with Actix and Shuttle

This project is a simple **CRUD (Create, Read, Update, Delete) web server** built using [Actix Web](https://actix.rs/), a fast and powerful web framework for Rust, and hosted using [Shuttle](https://www.shuttle.rs/), a Rust-native deployment platform. This server provides basic CRUD operations via RESTful APIs, ideal for learning and rapid prototyping with Rust.

## Table of Contents

1. [Project Overview](#project-overview)
2. [Features](#features)
3. [Installation](#installation)
4. [Usage](#usage)
5. [API Endpoints](#api-endpoints)
6. [Screenshots](#screenshots)

## Project Overview

This web server provides CRUD operations for a sample resource (e.g., `Todo`, `Post`, or `User`). Each operation is handled through RESTful endpoints, allowing for easy data manipulation over HTTP. By combining Actix Web for efficient request handling and Shuttle for seamless deployment, this project demonstrates a complete backend setup in Rust.

## Features

- **Create**: Add new entries to the database.
- **Read**: Retrieve and display entries.
- **Update**: Modify existing entries.
- **Delete**: Remove entries.
- **Rust-native Deployment**: Deployed using Shuttle, making it accessible online without extra infrastructure.

## Installation

To set up the project locally, make sure you have [Rust](https://www.rust-lang.org/) installed. 

1. **Clone the repository**:
   ```bash
   git clone https://github.com/toastx/actix-shuttle-crud
   cd actix-shuttle-crud
   ```

2. **Set up dependencies**:
   This project uses Actix Web for the server and Shuttle for deployment.
   ```bash
   make install
   ```

3. **Set up environment variables**:
   Configure environment variables for database credentials and other sensitive information by creating a `.env` file.

4. **Run the server**:
   ```bash
   make run
   ```
5. **Deploy to Shuttle**:
   Once tested locally, you can deploy the server to Shuttle for a live instance.
   ```bash
   cargo shuttle deploy
   ```
## Usage

After starting the server, you can access it locally at `http://127.0.0.1:8000` or at your Shuttle-deployed URL. 

## API Endpoints

Here are the endpoints for the CRUD operations, using a sample resource called `Todo`:

| Method | Endpoint                | Description                  | Example Request Body  |
|--------|--------------------------|------------------------------|-----------------------|
| GET    | `/api/todos`             | Retrieve all todos          | N/A                   |
| GET    | `/api/todos/{id}`        | Retrieve a single todo      | N/A                   |
| POST   | `/api/todos`             | Create a new todo           | `{ "name": "Sample", "description": "A sample task", "completed": false }` |
| PUT    | `/api/todos/{id}`        | Update an existing todo     | `{ "completed": true }` |
| DELETE | `/api/todos/{id}`        | Delete a todo               | N/A                   |

These endpoints return JSON-formatted responses for each operation.

## Screenshots

Here are examples of the CRUD API endpoints in action. Replace each placeholder below with a screenshot of your choice.

### 1. Creating a Todo
![image](https://github.com/user-attachments/assets/345ad91c-9fa7-4b56-9a3e-5c25f76f5a19)

### 2. Retrieving Todos
![image](https://github.com/user-attachments/assets/e8e43ff8-d2ac-40e0-9997-20b8066bca24)


### 3. Retrieving a Single Todo
![image](https://github.com/user-attachments/assets/2c202248-7f0e-4dc7-95ca-d7b57ec0b2aa)


### 4. Updating a Todo
![image](https://github.com/user-attachments/assets/c6e0b9a5-4114-46cb-ba5c-ea3c1f7b4515)


### 5. Deleting a Todo
![image](https://github.com/user-attachments/assets/3dc186bb-447b-4116-a5cc-19be86f029e4)


