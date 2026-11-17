# Ex03 To-Do List using JavaScript
## Date:

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


## OUTPUT


## RESULT
The program for creating To-do list using JavaScript is executed successfully.
