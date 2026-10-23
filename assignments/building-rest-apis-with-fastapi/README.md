# 📘 Assignment: Building REST APIs with FastAPI

## 🎯 Objective

Build a small REST API with FastAPI to manage a collection of books. Practice defining HTTP endpoints, accepting and validating JSON data, and returning appropriate responses and status codes.

## 📝 Tasks

### 🛠️ Create the API and List Books

#### Description
Create a Python application with a FastAPI instance for a book collection. Run it locally with Uvicorn and explore the automatically generated API documentation.

#### Requirements
Completed program should:

- Install FastAPI and Uvicorn and start the application with `uvicorn main:app --reload`
- Define a `GET /books` endpoint that returns a JSON array of books (an empty array is acceptable initially)
- Define a `GET /health` endpoint that returns a JSON response indicating the API is running
- Open `/docs` in a browser and confirm both endpoints appear in the interactive documentation


### 🛠️ Add Books with Validated Data

#### Description
Allow clients to add books to the collection by sending a JSON request. Use a Pydantic model to validate each book's data.

#### Requirements
Completed program should:

- Define a book model with a non-empty `title`, a non-empty `author`, and a `year` between 1 and the current year
- Implement `POST /books` to accept a book as JSON and add it to the collection
- Return the created book and an appropriate success status code
- Verify that invalid or missing field values are rejected with a validation error


### 🛠️ Manage Books by ID

#### Description
Give every book a unique ID and implement endpoints to look up, update, and remove a book. Keep the collection in memory; it is acceptable for it to reset when the application restarts.

#### Requirements
Completed program should:

- Implement `GET /books/{book_id}` to return one book
- Implement `PUT /books/{book_id}` to update a book's data
- Implement `DELETE /books/{book_id}` to remove a book
- Return an HTTP 404 response when a requested book ID does not exist
- Test the create, read, update, and delete operations using `/docs`
