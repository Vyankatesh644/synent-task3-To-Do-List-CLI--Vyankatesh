# 📋 To Do List (CLI)

A simple Command Line Task Manager built using Python.  
This application allows users to add, view, and delete tasks using a menu-driven interface.

---

## 📌 Features

✔ Add Tasks  
✔ View Tasks  
✔ Delete Tasks  
✔ Menu-Driven Interface  
✔ User-Friendly CLI  
✔ Error Handling for Invalid Inputs  

---

## 🚀 Technologies Used

- Python 3

---

## 📂 Project Structure

```bash
simple-task-manager/
│
├── task_manager.py
└── README.md
```

---

## ▶ How to Run the Project

### 1️⃣ Clone the Repository

```bash
git clone https://github.com/your-username/simple-task-manager.git
```

### 2️⃣ Navigate to the Project Folder

```bash
cd simple-task-manager
```

### 3️⃣ Run the Program

```bash
python task_manager.py
```

---

## 💻 Program Code

```python
# Simple Task Manager

tasks = []

while True:
    print("\n===== TASK MANAGER =====")
    print("1. Add Task")
    print("2. View Tasks")
    print("3. Delete Task")
    print("4. Exit")

    choice = input("Enter your choice: ")

    # Add Task
    if choice == "1":
        task = input("Enter new task: ")
        tasks.append(task)
        print("Task added successfully!")

    # View Tasks
    elif choice == "2":
        if len(tasks) == 0:
            print("No tasks available.")
        else:
            print("\nYour Tasks:")
            for index, task in enumerate(tasks, start=1):
                print(f"{index}. {task}")

    # Delete Task
    elif choice == "3":
        if len(tasks) == 0:
            print("No tasks to delete.")
        else:
            print("\nTasks:")
            for index, task in enumerate(tasks, start=1):
                print(f"{index}. {task}")

            try:
                task_num = int(input("Enter task number to delete: "))

                if 1 <= task_num <= len(tasks):
                    removed = tasks.pop(task_num - 1)
                    print(f"Task '{removed}' deleted successfully!")
                else:
                    print("Invalid task number.")

            except ValueError:
                print("Please enter a valid number.")

    # Exit
    elif choice == "4":
        print("Exiting Task Manager...")
        break

    # Invalid Choice
    else:
        print("Invalid choice! Please try again.")
```

---

## 📸 Example Output

```bash
===== TASK MANAGER =====
1. Add Task
2. View Tasks
3. Delete Task
4. Exit

Enter your choice: 1
Enter new task: Complete Python Project

Task added successfully!
```

### Viewing Tasks

```bash
Your Tasks:
1. Complete Python Project
2. Practice DSA
```

### Deleting Tasks

```bash
Enter task number to delete: 1

Task 'Complete Python Project' deleted successfully!
```

---

## ⚠ Error Handling

The program handles:

- Invalid menu choices
- Invalid task numbers
- Non-numeric inputs during deletion

Example:

```bash
Please enter a valid number.
```

---

## 📚 Concepts Used

- Lists
- Loops
- Conditional Statements
- User Input
- Exception Handling
- List Operations
- Enumerate Function

---

## 🔮 Future Improvements

- Mark tasks as completed ✅
- Save tasks to a file
- Add task deadlines
- Add task priorities
- GUI version using Tkinter
- Database integration

---

## 🤝 Contributing

Contributions are welcome.  
Feel free to fork this repository and improve the project.

---

## 📜 License

This project is open-source and available under the MIT License.

