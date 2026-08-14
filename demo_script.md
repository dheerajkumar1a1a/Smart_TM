# 10-Minute Demo Script

## 0:00–0:45 — Introduction

"Hello, this is my Smart Task Management System. The objective of the project is to provide a simple interface where users can create, manage, search and track their daily tasks.

I intentionally kept the architecture simple using HTML, CSS and JavaScript, with browser localStorage for persistence."

## 0:45–1:30 — Project Architecture

"At a high level, the application is client-side. HTML creates the interface, CSS handles styling and responsive design, and JavaScript handles the application logic.

The task data is stored in localStorage as JSON. This removes the need for a separate database for this basic version."

Show `architecture.svg`.

## 1:30–2:30 — Add Task

Demonstrate:
1. Enter a task.
2. Select priority.
3. Select category.
4. Select a due date.
5. Click Add Task.

Say:

"When I click Add Task, JavaScript reads the form values and creates a task object containing an ID, name, priority, category, due date and completion status."

## 2:30–3:30 — View, Complete and Delete

Demonstrate the task list.

Click Complete.

Say:

"The completed state is stored in the task object. The interface visually changes the task and the dashboard statistics are updated."

Then demonstrate Delete.

Say:

"Delete removes the selected task from the array and localStorage."

## 3:30–4:30 — Edit

Click Edit.

Say:

"The edit function finds the task using its unique ID and updates the task name or priority. The updated data is then saved again."

## 4:30–5:30 — Search and Filtering

Use the search field.

Then demonstrate:
- All Tasks
- Pending
- Completed
- High Priority

Say:

"The filtering is performed in JavaScript. Search checks whether the task name contains the entered text, while the dropdown applies status or priority filters."

## 5:30–6:15 — Dashboard

Point to:
- Total Tasks
- Pending
- Completed
- High Priority

Say:

"The dashboard is calculated dynamically from the current task array. This means the statistics automatically change when tasks are added, completed or deleted."

## 6:15–7:30 — Smart Task Assistant

Click Generate AI Suggestion.

Say:

"The application also contains a smart task recommendation feature. To keep the project beginner-friendly and completely client-side, I implemented a rule-based recommendation algorithm.

It first considers pending tasks, then prioritizes High over Medium over Low. If priority is the same, it uses the earlier due date."

Important wording:

"I would describe this as an intelligent or AI-style recommendation feature rather than claiming it is a generative AI model. A future version could connect this feature to an LLM through a secure backend."

## 7:30–8:15 — Dark Mode and Responsive Design

Click Dark Mode.

Resize the browser or show the mobile layout.

Say:

"I also added dark mode and responsive CSS so the interface remains usable on smaller screens."

## 8:15–9:00 — Data Persistence

Refresh the page.

Say:

"After refreshing, the tasks remain available because they are stored in localStorage. The browser stores the task array as JSON and loads it again when the application starts."

## 9:00–9:40 — Design Decisions

Say:

"I chose Vanilla JavaScript rather than a framework because the assignment can be completed with a much smaller and easier-to-explain codebase.

I chose localStorage because the requirements allow local storage and it removes database configuration.

The application is also intentionally modular at the function level, with separate functions for adding, displaying, editing, deleting, completing and recommending tasks."

## 9:40–10:00 — Conclusion

"In summary, the application satisfies the core task-management requirements, provides persistent storage, search and filtering, dashboard statistics, dark mode and a smart task recommendation feature.

The next logical step would be to add a backend, user authentication, a cloud database and a real LLM integration through a secure server.

Thank you."
