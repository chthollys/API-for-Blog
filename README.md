# Blog API Project

This is a simple Blog API project built using Node.js and Express.js. The project provides a RESTful API for managing blog posts, including features to create, update, delete, and retrieve posts. It also includes a frontend server for rendering the blog posts and forms for adding or editing them.

## Features

### API Features
- **GET /posts**: Retrieve all blog posts.
- **GET /posts/:id**: Retrieve a specific blog post by ID.
- **POST /posts**: Create a new blog post.
- **PATCH /posts/:id**: Update specific fields of a blog post.
- **DELETE /posts/:id**: Delete a blog post by ID.

### Frontend Features
- Display all blog posts on the main page.
- Create a new blog post using a form.
- Edit an existing blog post using a form.
- Delete a blog post from the frontend.

## Project Structure

```
.
├── index.js          # Main API server
├── server.js         # Frontend server
├── package.json      # Project dependencies and scripts
├── package-lock.json # Dependency lockfile
├── public/           # Static assets (CSS, JavaScript, etc.)
├── views/            # EJS templates for frontend rendering
```

## Requirements

- Node.js (v14 or higher)
- npm (v6 or higher)

## Installation

1. Clone the repository:
   ```bash
   git clone <repository-url>
   cd <repository-folder>
   ```

2. Install dependencies:
   ```bash
   npm install
   ```

## Usage

### Starting the API Server
Run the API server (on port 4000):
```bash
node index.js
```

### Starting the Frontend Server
Run the frontend server (on port 3000):
```bash
node server.js
```

### Accessing the Application
- API: `http://localhost:4000`
- Frontend: `http://localhost:3000`

## API Endpoints

### **GET /posts**
Retrieve all blog posts.
- **Response:** JSON array of blog posts.

### **GET /posts/:id**
Retrieve a single blog post by its ID.
- **Response:** JSON object of the post.

### **POST /posts**
Create a new blog post.
- **Request Body:**
  ```json
  {
    "title": "Post Title",
    "content": "Post content",
    "author": "Author Name",
    "date": "YYYY-MM-DD"
  }
  ```
- **Response:** JSON object of the created post.

### **PATCH /posts/:id**
Update specific fields of a blog post.
- **Request Body:** Any combination of:
  ```json
  {
    "title": "New Title",
    "content": "Updated content",
    "author": "New Author"
  }
  ```
- **Response:** JSON object of the updated post.

### **DELETE /posts/:id**
Delete a blog post by its ID.
- **Response:** Confirmation message.

## Dependencies

The project uses the following npm packages:

- **express**: Web framework for building APIs and servers.
- **body-parser**: Middleware for parsing request bodies.
- **axios**: HTTP client for making requests between servers.
- **ejs**: Template engine for rendering views.
- **nodemon**: Utility to automatically restart the server during development.