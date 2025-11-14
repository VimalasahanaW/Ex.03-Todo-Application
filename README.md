# Ex03 To-Do List using JavaScript
## Name : VIMALA SAHANA W
## Reg No: 212223040241

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
### Index.html
```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Todo Application</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>
    <div class="container">
        <h1>Todo Application</h1>
        <div class="input-section">
            <input type="text" id="todo-input" placeholder="Add a new task">
            <button id="add-btn">Add</button>
        </div>
        <ul id="todo-list"></ul>
    </div>

    <!-- Include JavaScript at the end so HTML elements are loaded -->
    <script src="script.js"></script>
</body>
</html>

```
### Style.css
```
body {
    font-family: Arial, sans-serif;
    background: #f4f4f4;
    display: flex;
    justify-content: center;
    align-items: center;
    height: 100vh;
}

.container {
    background: #fff;
    padding: 20px 30px;
    border-radius: 10px;
    box-shadow: 0 5px 15px rgba(0,0,0,0.1);
    width: 400px;
}

h1 {
    text-align: center;
    color: #333;
}

.input-section {
    display: flex;
    margin-bottom: 20px;
}

#todo-input {
    flex: 1;
    padding: 10px;
    border: 1px solid #ddd;
    border-radius: 5px 0 0 5px;
    outline: none;
}

#add-btn {
    padding: 10px 20px;
    border: none;
    background: #28a745;
    color: #fff;
    border-radius: 0 5px 5px 0;
    cursor: pointer;
}

#add-btn:hover {
    background: #218838;
}

ul {
    list-style-type: none;
    padding: 0;
}

li {
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding: 10px 5px;
    border-bottom: 1px solid #ddd;
}

li.completed span {
    text-decoration: line-through;
    color: gray;
}

button.edit-btn, button.delete-btn {
    margin-left: 5px;
    border: none;
    padding: 5px 8px;
    cursor: pointer;
    border-radius: 3px;
}

button.edit-btn {
    background: #ffc107;
    color: #fff;
}

button.edit-btn:hover {
    background: #e0a800;
}

button.delete-btn {
    background: #dc3545;
    color: #fff;
}

button.delete-btn:hover {
    background: #c82333;
}

  ```
### Script.js
```
// Select elements
const todoInput = document.getElementById('todo-input');
const addBtn = document.getElementById('add-btn');
const todoList = document.getElementById('todo-list');

// Add todo
addBtn.addEventListener('click', () => {
    const task = todoInput.value.trim();
    if (task === "") {
        alert("Please enter a task!");
        return;
    }

    // Create a new list item
    const li = document.createElement('li');
    li.textContent = task;

    // Add click to mark completed
    li.addEventListener('click', () => {
        li.classList.toggle('completed');
    });

    // Add li to ul
    todoList.appendChild(li);

    // Clear input
    todoInput.value = "";
});

  ```

## OUTPUT:
<img width="1919" height="977" alt="Screenshot 2025-11-14 155524" src="https://github.com/user-attachments/assets/38ba1532-2267-4bf4-bba9-8c35737add33" />


## RESULT
The program for creating To-do list using JavaScript is executed successfully.
