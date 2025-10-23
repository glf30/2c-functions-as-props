# Exercise - Functions as Props

## Exercise Overview

We are going to create a simple task manager application that displays a list of tasks and includes buttons to mark tasks as complete or delete them. We'll iterate over an array of tasks using manual mapping, and we'll pass the task title as a parameter to the complete function.

## Set Up And Run A New React App

1. Open the terminal to the `exercise` directory--the simplest way to do so is to right-click on the `exercise` folder in VS Code and select "Open in Integrated Terminal".

2. In the terminal, type `npm create vite .` and hit enter/return. The `.` is important--this will create a new Vite project in the current directory.

3. It will warn you that there are files here currently. Use the arrow keys and Enter/Return to select "Ignore files and continue". This allows us to keep our readme and any data/assets files we have in our new project folder.

4. Choose React and then JavaScript from the following menus, using arrow keys and Enter/Return.

5. Install dependencies by entering `npm install` in the terminal.

6. Run the app by typing `npm run dev` in the terminal. This will provide a clickable link to open the app in your default browser, or you can navigate to the localhost URL in your browser.

## Creating the App Component

Open /src/App.jsx. This file is an example component that Vite starts us with. You can delete everything in this file. Then at the top of the file, you can create a functional component named App. Don't forget to export it.

Create a `<div>` inside of the return() statement.

```jsx
function App() {
  return <div></div>;
}

export default App;
```

Then inside the `<div>` create a heading `<h1>Task Manager</h1>`.

```jsx
function App() {
  return (
    <div>
      <h1>Task Manager</h1>
    </div>
  );
}
```

Save the file and visit the browser to make sure our heading is appearing.

Back inside /src/App.jsx, below our heading, place a <div>.

```jsx
function App() {
  return (
    <div>
      <h1>Task Manager</h1>
      <div></div>
    </div>
  );
}
```

## Creating the Task Component

In VS Code, in the File Explorer to the left, right-click on the /src/ folder and select New File. Name the file Task.jsx.

Open /src/Task.jsx and create a function called Task that returns a `<div>` inside of parentheses. Don't forget to export the function at the bottom of the file.

Inside the `div`, let's write some placeholder text: `This is a Task.`

```jsx
function Task() {
  return <div>This is a Task</div>;
}

export default Task;
```

Let's try to import this Task into our App component. Open /src/App.jsx again and after importing React, create a new line to import our Task: `import Task from './Task';`

Then, inside of the `<div>`, render your Task component with `<Task />`.

```jsx
import Task from "./Task";

function App() {
  return (
    <div>
      <h1>Task Manager</h1>
      <div>
        <Task />
      </div>
    </div>
  );
}

export default App;
```

Save and check the browser. You should see the text: "This is a Task"

## Passing Functions as Props and Iterating Manually
Create an array of tasks.  A task should consist of an **id**, **title**, and **description**.

Let's use props to pass functions from our App component to our Task component. We will create functions to mark tasks as complete and delete them. We'll also iterate over an array of tasks manually.

Open /src/App.jsx and create two functions to handle actions: `completeTask` and `deleteTask`. Both should take in the task title as a parameter and alert the user that the task has been completed or deleted.  

## Updating the Task Component
Your task compnent should display the title and description of the task.  It should also include buttons for completing and deleting the task.  These buttons should access the `completeTask` and `deleteTask` functions in the parent component and execute based on the button clicked
