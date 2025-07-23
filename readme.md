# Task Manager API

This is a simple RESTful API built using Flask and SQLite. It allows users to create, read, update, and delete tasks. I made this as part of my internship Task 1.

## Setup Instructions

1. Create a virtual environment:
>> python -m venv env
2. Activate the environment:
>> .\env\Scripts\activate
3. Install the dependencies:
>> pip install -r requirements.txt
4. Run the database setup file:
>> python create_db.py
5. Start the Flask server:
>> python app.py

## API Endpoints

### Base URL:
http://127.0.0.1:5000/

### Routes:

"GET /tasks"
- Returns all tasks.

"POST /tasks"
  Creates a new task. Requires JSON in this format:
{
  "title": "Task title",
  "description": "Task description"
}

"PUT /tasks/<id>"
Updates an existing task. JSON format:
{
  "title": "Updated title",
  "description": "Updated description",
  "done": true
}

"DELETE /tasks/<id>"
Deletes the task with the given ID.

Notes:
I used Postman to test all the API routes.

The database used is SQLite and the file is named database.db.

All models are defined in models.py and the database is initialized in extensions.py.