# Task Management API

# Set Up:

Create the virtual environment by using:
pip -m venv .venv
.venv\Scripts\activate

# Install Dependecies by:
pip install -r requirements.txt

# Do Migrations:
python manage.py makemigrations: Create Migration files
python manage.py migrate: do all the changes in the database

# Create superuser so that we access the admin panel:
python manage.py createsuperuser

Method -> Endpoint ->	               Description

POST   -> /api/tasks/create/	    Create a new task

PUT	   -> /api/tasks/task_id/assign/	Assign users to a task

GET	   -> /api/tasks/user/id/	    Get tasks for a specific user

For Create Task:

Endpoint: POST /api/tasks/create/

Payload:

{
  "name": "Design API",
  "description": "Create API for task management",
  "task_type": "Backend",
  "status": "pending"
}

Assign Task to Users

Endpoint: PUT /api/tasks/1/assign/

{
  "assigned_users": [1]
}

Retrieve Tasks for a User

Endpoint: GET /api/tasks/user/1/
