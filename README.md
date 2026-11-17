# Ex03 To-Do List using JavaScript
## Date:17-11-2026

## AIM
To create a To-do Application with all features using JavaScript.

## ALGORITHM
### STEP 1
Build the HTML structure (index.html).

### STEP 2
Style the App (style.css).

### STEP 3
Plan the features the To-Do App should have.

### STEP 4
Create a To-do application using Javascript.

### STEP 5
Add functionalities.

### STEP 6
Test the App.

### STEP 7
Open the HTML file in a browser to check layout and functionality.

### STEP 8
Fix styling issues and refine content placement.

### STEP 9
Deploy the website.

### STEP 10
Upload to GitHub Pages for free hosting.

## PROGRAM

index.html

```

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>TaskFlow Dashboard</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>

<div class="dashboard">

    <!-- Sidebar -->
    <aside class="sidebar">
        <h2>TaskFlow</h2>

        <nav>
            <a href="#">📥 Inbox</a>
            <a href="#">☆ Today</a>
            <a href="#">📅 Upcoming</a>
            <a href="#">▢ Anytime</a>
            <a href="#">▣ Someday</a>
            <a href="#">🗑 Trash</a>
        </nav>

        <h3>MY LISTS</h3>
        <nav>
            <a href="#">🔴 Family</a>
            <a href="#">🟡 Vacation Planning</a>
            <a href="#">🔵 Buy a new car</a>
            <a href="#">🟢 Festival Ideas</a>
        </nav>

        <h3>WORK</h3>
        <nav>
            <a href="#">Onboarding Plan</a>
            <a href="#">Project Review</a>
            <a href="#">Presentation Work</a>
        </nav>
    </aside>

    <!-- Main Content -->
    <main class="main-content">

        <header>
            <h1>Today Task</h1>
            <p>Manage your daily activities</p>
        </header>

        <div class="tabs">
            <span>All</span>
            <span>Important</span>
            <span>Notes</span>
            <span>Links</span>
        </div>

        <div class="add-task">
            <input type="text" id="taskInput" placeholder="Add a new task...">
            <button onclick="addTask()">+ Add</button>
        </div>

        <ul id="taskList">
            <li>
                <input type="checkbox">
                <span>Create website design</span>
                <small>In Progress</small>
            </li>
            <li>
                <input type="checkbox">
                <span>Complete project report</span>
                <small>Waiting</small>
            </li>
            <li>
                <input type="checkbox">
                <span>Prepare presentation</span>
                <small>Approved</small>
            </li>
        </ul>

        <h2 class="upcoming-title">Upcoming Tasks</h2>
        <p class="upcoming-text">Your upcoming activities will appear here.</p>

    </main>

    <!-- Right Panel -->
    <aside class="right-panel">

        <h2>Meetings Schedule</h2>

        <div class="meeting yellow">
            <small>08:45 AM - 9:20 AM</small>
            <h3>Team Meeting</h3>
            <p>Project Discussion</p>
        </div>

        <div class="meeting blue">
            <small>10:05 AM - 12:20 PM</small>
            <h3>Development Team</h3>
            <p>Project Development</p>
        </div>

        <div class="meeting pink">
            <small>03:00 PM - 04:20 PM</small>
            <h3>Product Planning</h3>
            <p>Weekly Planning</p>
        </div>

    </aside>

</div>

<script src="script.js"></script>
</body>
</html>
```

style.css

```

* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

body {
    font-family: 'Segoe UI', Arial, sans-serif;
    background: #e9edf5;
    color: #292d36;
}

.dashboard {
    display: grid;
    grid-template-columns: 220px 1fr 300px;
    max-width: 1450px;
    min-height: 95vh;
    margin: 20px auto;
    background: white;
    border-radius: 18px;
    overflow: hidden;
    box-shadow: 0 10px 35px rgba(0,0,0,0.08);
}

/* Sidebar */

.sidebar {
    background: #f7f8fc;
    padding: 35px 22px;
    border-right: 1px solid #eeeeee;
}

.sidebar h2 {
    font-size: 25px;
    color: #5b45d6;
    margin-bottom: 35px;
}

.sidebar h3 {
    font-size: 12px;
    color: #999;
    margin: 30px 0 12px;
    letter-spacing: 1px;
}

.sidebar nav {
    display: flex;
    flex-direction: column;
    gap: 8px;
}

.sidebar nav a {
    text-decoration: none;
    color: #555b68;
    font-size: 14px;
    padding: 10px;
    border-radius: 8px;
    transition: 0.3s;
}

.sidebar nav a:hover {
    background: #eae6ff;
    color: #6247d8;
}

/* Main Content */

.main-content {
    padding: 40px 35px;
}

.main-content header h1 {
    font-size: 28px;
    margin-bottom: 8px;
}

.main-content header p {
    color: #999;
    font-size: 14px;
}

.tabs {
    display: flex;
    justify-content: space-between;
    gap: 15px;
    margin: 35px 0 25px;
    padding-bottom: 15px;
    border-bottom: 1px solid #eee;
}

.tabs span {
    font-size: 14px;
    color: #777;
    cursor: pointer;
    padding-bottom: 10px;
}

.tabs span:first-child {
    color: #6247d8;
    border-bottom: 2px solid #6247d8;
}

/* Add Task */

.add-task {
    display: flex;
    gap: 10px;
    margin-bottom: 25px;
}

.add-task input {
    flex: 1;
    min-width: 0;
    padding: 12px;
    border: 1px solid #ddd;
    border-radius: 8px;
    outline: none;
    font-size: 14px;
}

.add-task input:focus {
    border-color: #7055dc;
}

.add-task button {
    padding: 12px 17px;
    background: #684ee0;
    color: white;
    border: none;
    border-radius: 8px;
    cursor: pointer;
}

.add-task button:hover {
    background: #5138c5;
}

/* Task List */

#taskList {
    list-style: none;
}

#taskList li {
    display: flex;
    align-items: center;
    gap: 12px;
    padding: 17px 5px;
    border-bottom: 1px solid #f0f0f0;
    font-size: 14px;
}

#taskList li input {
    width: 16px;
    height: 16px;
    accent-color: #684ee0;
    cursor: pointer;
}

#taskList li span {
    flex: 1;
}

#taskList li small {
    background: #e6f8f2;
    color: #32a88a;
    padding: 6px 10px;
    border-radius: 20px;
    font-size: 11px;
}

/* Upcoming Tasks */

.upcoming-title {
    font-size: 20px;
    margin-top: 45px;
    margin-bottom: 15px;
}

.upcoming-text {
    color: #999;
    font-size: 13px;
}

/* Right Panel */

.right-panel {
    padding: 40px 25px;
    border-left: 1px solid #eee;
}

.right-panel h2 {
    font-size: 20px;
    margin-bottom: 30px;
}

.meeting {
    padding: 22px 18px;
    border-radius: 12px;
    margin-bottom: 20px;
    min-height: 125px;
}

.meeting small {
    font-size: 11px;
    color: #777;
}

.meeting h3 {
    font-size: 15px;
    margin: 12px 0 7px;
}

.meeting p {
    font-size: 12px;
    color: #666;
}

.yellow {
    background: #fff2d5;
}

.blue {
    background: #dcecff;
}

.pink {
    background: #ffdddd;
}

/* Responsive Design */

@media (max-width: 1000px) {
    .dashboard {
        grid-template-columns: 190px 1fr;
    }

    .right-panel {
        grid-column: 2;
        border-left: none;
        border-top: 1px solid #eee;
    }
}

@media (max-width: 650px) {
    .dashboard {
        display: flex;
        flex-direction: column;
        margin: 0;
        border-radius: 0;
    }

    .sidebar {
        padding: 20px;
    }

    .sidebar nav {
        flex-direction: row;
        flex-wrap: wrap;
    }

    .main-content,
    .right-panel {
        padding: 25px 18px;
    }

    .tabs {
        gap: 12px;
        flex-wrap: wrap;
    }
}

.edit-btn,
.delete-btn {
    border: none;
    padding: 7px 10px;
    border-radius: 6px;
    cursor: pointer;
    font-size: 12px;
}

.edit-btn {
    background: #e8e3ff;
    color: #6247d8;
}

.delete-btn {
    background: #ffe5e5;
    color: #e05252;
}

.edit-btn:hover {
    background: #d9d0ff;
}

.delete-btn:hover {
    background: #ffd0d0;
}

#taskList li {
    flex-wrap: wrap;
}
```
script.js

```

let tasks = JSON.parse(localStorage.getItem("tasks")) || [];

const taskInput = document.getElementById("taskInput");
const taskList = document.getElementById("taskList");

function saveTasks() {
    localStorage.setItem("tasks", JSON.stringify(tasks));
}

function renderTasks() {
    taskList.innerHTML = "";

    tasks.forEach((task, index) => {
        let li = document.createElement("li");

        let checkbox = document.createElement("input");
        checkbox.type = "checkbox";
        checkbox.checked = task.completed;

        checkbox.addEventListener("change", () => {
            tasks[index].completed = checkbox.checked;
            saveTasks();
            renderTasks();
        });

        let span = document.createElement("span");
        span.textContent = task.name;

        if (task.completed) {
            span.style.textDecoration = "line-through";
            span.style.color = "#999";
        }

        let status = document.createElement("small");
        status.textContent = task.completed ? "Completed" : "In Progress";

        let editBtn = document.createElement("button");
        editBtn.textContent = "Edit";
        editBtn.className = "edit-btn";

        editBtn.onclick = () => {
            let newName = prompt("Edit your task:", task.name);

            if (newName !== null && newName.trim() !== "") {
                tasks[index].name = newName.trim();
                saveTasks();
                renderTasks();
            }
        };

        let deleteBtn = document.createElement("button");
        deleteBtn.textContent = "Delete";
        deleteBtn.className = "delete-btn";

        deleteBtn.onclick = () => {
            tasks.splice(index, 1);
            saveTasks();
            renderTasks();
        };

        li.appendChild(checkbox);
        li.appendChild(span);
        li.appendChild(status);
        li.appendChild(editBtn);
        li.appendChild(deleteBtn);

        taskList.appendChild(li);
    });
}

function addTask() {
    let name = taskInput.value.trim();

    if (name === "") {
        alert("Please enter a task!");
        return;
    }

    tasks.push({
        name: name,
        completed: false
    });

    taskInput.value = "";

    saveTasks();
    renderTasks();
}

taskInput.addEventListener("keypress", function(event) {
    if (event.key === "Enter") {
        addTask();
    }
});

renderTasks();
```


## OUTPUT

![alt text](<Screenshot 2026-11-17 132607.png>)


## RESULT
The program for creating To-do list using JavaScript is executed successfully.
