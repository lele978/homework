# Todo Task Manager

This project is a simple Bash script to manage your todo tasks. The script allows you to create, update, delete, view, list, and search tasks. Each task has a unique identifier, a title, a description, a location, a due date, and a completion status.

## Features

- Create a new task with a unique identifier.
- Update the fields of an existing task.
- Delete a task by its identifier.
- Show all information about a specific task.
- List tasks of a given day, separating completed and uncompleted tasks.
- Search for tasks by their title.
- When run without arguments, display tasks of the current day, separating completed and uncompleted tasks.

## Design Choices

### Data Storage

Tasks are stored in a plain text file named `tasks.txt`. Each line in this file represents a single task, with fields separated by tabs. The fields are:

1. Task ID
2. Title
3. Description
4. Location
5. Due Date (in YYYY-MM-DD format)
6. Completion Status (either "completed" or "uncompleted")

### Code Organization

The script is organized into several functions, each responsible for a specific feature:

- `create_task`: Prompts the user for task details and appends a new task to `tasks.txt`.
- `update_task`: Prompts the user for a task ID and the field to update, then modifies the specified task.
- `delete_task`: Prompts the user for a task ID and deletes the corresponding task from `tasks.txt`.
- `task_info`: Prompts the user for a task ID and displays the details of the specified task.
- `list_tasks`: Prompts the user for a date and lists tasks for that date, separated into completed and uncompleted sections.
- `search_task_by_title`: Prompts the user for a title and lists tasks with matching titles.
- `show_help`: Displays usage instructions for the script.

### Input Validation

The script validates user inputs to ensure required fields are not empty and dates are in the correct format. Error messages are redirected to standard error to separate them from regular output.

## How to Run the Program

### Prerequisites

- A Unix-like operating system with Bash installed.
- `awk` and `date` utilities (commonly available on Unix-like systems).

### Steps

1. Clone the repository to your local machine:

   ```bash
   git clone https://github.com/yourusername/todo-task-manager.git
   cd todo-task-manager
