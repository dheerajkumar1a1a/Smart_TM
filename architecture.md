# Architecture

The project follows a simple client-side architecture.

```text
User
  |
  v
index.html
  |
  +-------------------+
  |                   |
  v                   v
HTML UI             CSS UI
  |
  v
JavaScript Application Logic
  |
  +----------+-----------+-------------+
  |          |           |             |
  v          v           v             v
CRUD      Search/     Dashboard     Smart Task
Tasks     Filters     Statistics    Suggestion
  |                                      |
  +------------------+-------------------+
                     |
                     v
              Browser localStorage
```

## Components

### 1. User Interface
HTML provides the task form, dashboard, filters, buttons and task cards.

### 2. Styling
CSS provides layout, responsive behavior and dark mode.

### 3. Application Logic
JavaScript manages the task array and implements CRUD operations, filtering, dashboard calculations and the smart recommendation algorithm.

### 4. Persistence
Browser localStorage stores the task array as JSON.

### 5. Smart Feature
The recommendation function ranks pending tasks by priority and then due date.

## Data Flow

```text
Add Task
   |
   v
Create JavaScript object
   |
   v
tasks[] array
   |
   v
JSON.stringify()
   |
   v
localStorage
   |
   v
displayTasks()
   |
   v
Updated UI
```
