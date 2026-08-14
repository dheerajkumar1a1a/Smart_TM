# Smart Task Management System

A simple beginner-friendly task management web application built using **HTML, CSS and JavaScript**. It requires no backend or installation and stores task data in the browser using `localStorage`.

## Features

### Mandatory
- Add a new task
- View all tasks
- Edit an existing task
- Delete a task
- Mark tasks as Completed/Pending
- Search and filter tasks
- Persist task data using browser localStorage
- Smart task suggestion feature

### Additional
- Task priority: Low / Medium / High
- Categories: Work / Study / Personal / Other
- Due dates
- Dashboard statistics
- Dark mode
- Responsive layout

## Technology Stack

- HTML5 — page structure
- CSS3 — styling and responsive layout
- Vanilla JavaScript — application logic
- Browser localStorage — data persistence

No framework, server, database installation or package manager is required.

## Project Structure

```text
SmartTaskManagementSystem/
├── index.html
├── README.md
├── architecture.svg
├── architecture.md
├── demo_script.md
├── DEPLOYMENT.md
├── screenshots/
│   ├── 01-dashboard.png
│   ├── 02-tasks-and-ai.png
│   └── 03-dark-mode.png
└── .gitignore
```

## Setup Instructions

1. Download or clone the repository.
2. Open the project folder.
3. Double-click `index.html`.

Alternatively, run a simple local server:

```bash
python -m http.server 8000
```

Then open:

```text
http://localhost:8000
```

## How the application works

The application keeps all tasks in a JavaScript array:

```javascript
let tasks = JSON.parse(localStorage.getItem("tasks")) || [];
```

When a task is added, edited, completed or deleted, the array is updated and saved:

```javascript
localStorage.setItem("tasks", JSON.stringify(tasks));
```

When the page opens again, the saved tasks are loaded from localStorage.

## CRUD Operations

| Operation | Function |
|---|---|
| Create | `addTask()` |
| Read | `displayTasks()` |
| Update | `editTask()` / `toggleComplete()` |
| Delete | `deleteTask()` |

## Smart Task Assistant

The project includes a lightweight intelligent recommendation feature. It selects the next task using:

1. Pending status
2. Priority
3. Due date

High-priority pending tasks are considered first. If priorities are equal, the earlier due date is preferred.

> Note: This implementation is a rule-based intelligent recommendation system rather than a cloud-based generative AI model. This keeps the project simple, secure and completely client-side. An actual LLM can be added later through a backend API without exposing an API key in the browser.

## Design Decisions

### Why Vanilla JavaScript?
The goal was to keep the project easy to understand and demonstrate. A framework such as React would add unnecessary complexity for a basic task manager.

### Why localStorage?
The mandatory requirement asks for a database or local storage. localStorage satisfies the requirement while avoiding database configuration.

### Why no backend?
The application is intentionally client-side so that it can run by opening one HTML file.

### Why rule-based AI?
It provides a meaningful smart suggestion without requiring an API key, server or external AI service. It can later be replaced with an LLM-backed recommendation service.

## Architecture

See `architecture.svg` and `architecture.md`.

## Screenshots

See the `screenshots/` directory.

## Deployment

The application can be deployed for free using GitHub Pages because it is a static HTML/CSS/JavaScript project. See `DEPLOYMENT.md`.

## Demo

A ready-to-follow 10-minute presentation script is provided in `demo_script.md`.

## Future Improvements

- Real LLM integration through a secure backend
- User authentication
- Cloud database
- Reminder notifications
- Email notifications
- Better edit form/modal
- Drag-and-drop task management
- Task analytics
- Deployment with a custom domain
