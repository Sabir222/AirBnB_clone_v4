# AirBnB Console Clone

This project is a simplified **AirBnB clone**, focused on building a command-line interface for managing project objects. Think of it as a custom shell designed specifically for handling users, places, and other related models.

---

## Introduction

**What is a command interpreter?**

If you’ve ever used a shell (like Bash), the idea is similar—except here the scope is restricted. Instead of handling system-wide commands, this interpreter lets you interact directly with the objects of the application.

You’ll be able to:

* Create new objects (e.g., `User`, `Place`)
* Retrieve stored objects from files or databases
* Perform actions on them (count, compute, etc.)
* Modify existing attributes
* Remove objects completely

---

## Learning Goals

By the end of this project, you should understand how to:

* Build a Python package from scratch
* Implement a command-line interpreter using the `cmd` module
* Write and run unit tests in a large codebase
* Serialize and deserialize classes
* Store and load data using JSON
* Work effectively with `datetime`
* Generate and use UUIDs
* Apply `*args` and `**kwargs` in practice
* Handle functions with named parameters

---

## Running the Console

The console works both interactively and non-interactively.

### Interactive mode:

```bash
$ ./console.py
(hbnb) help

Documented commands (type help <topic>):
========================================
EOF  help  quit

(hbnb) quit
$
```

### Non-interactive mode:

```bash
$ echo "help" | ./console.py
(hbnb)

Documented commands (type help <topic>):
========================================
EOF  help  quit
(hbnb)
$
```

You can also pipe files into the console:

```bash
$ cat test_help
help
$ cat test_help | ./console.py
(hbnb)

Documented commands (type help <topic>):
========================================
EOF  help  quit
(hbnb)
$
```

---

## Example Usage

**Start the console**

```bash
$ ./console.py
(hbnb)
```

**Create an object**

```bash
(hbnb) create
** class name missing **
(hbnb) create User
670265eb-5982-489e-8b92-2dff054f0776
```

**Show an object**

```bash
(hbnb) show User
** instance id missing **
(hbnb) show User 670265eb-5982-489e-8b92-2dff054f0776
[User] (670265eb-5982-489e-8b92-2dff054f0776) {'created_at': datetime.datetime(...), 'id': '670265eb-5982-489e-8b92-2dff054f0776', 'updated_at': datetime.datetime(...)}
```

**Update an object**

```bash
(hbnb) all
["[User] (70f71c16-962b-48ad-9df8-9203fe23d612) {...}"]

(hbnb) update
** class name missing **
(hbnb) update User
** instance id missing **
(hbnb) update User 70f71c16-962b-48ad-9df8-9203fe23d612
** attribute name missing **
(hbnb) update User 70f71c16-962b-48ad-9df8-9203fe23d612 Age "20"
(hbnb) all
["[User] (70f71c16-962b-48ad-9df8-9203fe23d612) {'Age': 20, ...}"]
```

**Delete an object**

```bash
(hbnb) destroy
** class name missing **
(hbnb) destroy User
** instance id missing **
(hbnb) destroy User 670265eb-5982-489e-8b92-2dff054f0776
(hbnb)
```

---

👉 This console is the first step in developing a complete AirBnB clone, forming the foundation for persistence, web APIs, and front-end integration later on.
