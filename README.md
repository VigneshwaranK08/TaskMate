# TaskMate 📝 
*A Python-based CLI Task Manager*  

[![Python](https://img.shields.io/badge/Python-3.x-blue?logo=python)](https://www.python.org/)  
[![License](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)  

A command-line task manager built with Python, Argparse, Tabulate and Datetime.  
It allows you to create, read, update, delete, sort, and mark tasks directly from the terminal.  
All tasks are stored locally in a JSON file 

---

“This project was built to strengthen my understanding of Python functions and the argparse module.”

## Features :

- Add tasks with optional details like description, status, and priority

- Easily update or modify existing tasks

- Track progress by marking tasks as todo, in-progress, or done

- View tasks in a table and sort them by status or priority

- Remove tasks individually or clear your entire task list
- Simple and intuitive CLI commands  
- JSON storage for easy management  

## 📦 Installation :

1. clone this repo anywhere
2. Give executable permission
3. create a Symlink of this repo to ~/.local/bin

```
> git clone https://VigneshwaranK08//TaskMate.git
> chmod +x TaskMate.py # ( after > cd TaskMate)
> sudo ln -s <path where u cloned> ~/.local/bin/taskmate
```


<details>
<summary>Click to view the usage guide</summary>

## Usage📖 :
Here are the main commands TaskMate supports:

- Add a Task

```
TaskMate add <TaskName> 
```
(optional)

```
TaskMate add <TaskName> -d <description> -s <status> -p <priority>
```
Note : status only accepts ['in-progress','done','todo'] defult = todo

Priority only accepts ["low","medium","high"] default="low"
- Update a Task

    - Update Name

    ```
    TaskMate update <TaskId> -n <NewTaskName>
    ```

    - Update Description

    ```
    TaskMate update <TaskId> -d <NewTaskDescription>
    ```

    - Update Priority

    ```
    TaskMate update <TaskId> -p <NewTaskPriority>
    ```
Note: All the above 3 flags can also be used at the same time 

- List Tasks 

    - List All Task

    ```
    TaskMate list
    ```

    - List Task Based on their Status

    ```
    TaskMate List done 
    ```

    ```
    TaskMate List in-progress 
    ```

    ```
    TaskMate List todo 
    ```

- Delete Task's

    - Delete Task By Providing Their Id

    ```
    TaskMate delete <TaskId>
    ```
    - Delete all Task

    ```
    TaskMate delete
    ```
- Change the Status of a Task

```
TaskMate mark <TaskId> <NewStatus>
```
The New Status only accepts done , todo , in-progress

- Veiw Sort the Tasks 

- Sort Tasks based on their Status
    - todo - in-progress -done

    ```
    TaskMate sort -s
    ```
    - done - in-progress - done

    ```
    TaskMate sort -S
    ```
- Sort Tasks based on their Priority
    - high - medium - low

    ```
    TaskMate sort -p
    ```
    - low - medium - high

    ```
    TaskMate sort -P
    ```
</details>

## Project Structure 📂:

```
TaskMate/
|-- TaskMate.py
|-- README.md
|-- .gitignore
|-- LICENSE
```

## 🙌 Acknowledgements

Special thanks to:

- [Roadmap.sh](https://roadmap.sh) → for project inspiration

- [RealPython](https://realpython.com/command-line-interfaces-python-argparse/) → for excellent Python tutorials