## Exercise: Task Manager App (Functions as Props)

Build a simple task manager that displays a list of tasks.
Each task should show its **title** and **description**, along with buttons to **complete** or **delete** the task.

This exercise focuses on **passing functions as props** and **manually iterating over data**.

### Requirements

* Create an `App` component that:

  * Displays a heading: **Task Manager**
  * Holds an array of tasks
    Each task should have:

    * `id`
    * `title`
    * `description`
  * Defines two functions:

    * `completeTask(title)`
    * `deleteTask(title)`
  * Each function should `alert` something like:

    * `"Completed [task title]"`
    * `"Deleted [task title]"`

* Create a `Task` component that:

  * Receives a single task as props
  * Displays:

    * The task title
    * The task description
    * A **Complete** button
    * A **Delete** button

* Pass the following from `App` to each `Task`:

  * The task data
  * The `completeTask` function
  * The `deleteTask` function

* When a button is clicked:

  * The appropriate function should be called from the parent
  * The task’s **title** should be passed as an argument

* Render multiple `Task` components by **manually mapping** over the tasks array in `App`
