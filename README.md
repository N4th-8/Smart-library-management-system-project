# Smart Library Management System

A menu-driven Object-Oriented Python application for managing a university library's books, members, and borrowing activity. Built as a group assignment for MCD4710 (Introduction to Programming).

## Overview

The system manages three types of library materials — printed books, e-books, and magazines — and supports two types of users: **Staff**, who manage the library's inventory, and **Members**, who borrow and return items.

## Features

**Staff can:**
- Add, edit, and delete library items
- View all items (sorted by title)
- Save all data to file

**Members can:**
- Register with name and contact number
- Borrow and return items
- View available items and their own borrowed items

**Core rules enforced:**
- Each item has a unique ID and can only be borrowed by one member at a time
- Borrowing durations differ by item type: printed books (14 days), e-books (7 days), magazines (3 days)
- Duplicate IDs, invalid input, and double-borrowing are all guarded against with error handling

## Object-Oriented Design

The project demonstrates:
- **Inheritance** — `PrintedBook`, `EBook`, and `Magazine` all inherit from an abstract `LibraryItem` base class
- **Polymorphism** — each item type applies its own borrowing duration and display behavior
- **Encapsulation** — internal data is accessed through class methods rather than exposed directly

Additional supporting classes: `Member` (tracks registered members and their borrowed items), `BorrowRecord` (tracks individual borrow/return transactions), and `Staff` (handles inventory management operations).

## Project structure

| File | Description |
|---|---|
| `main(Final Group Code).py` | Final, complete implementation of the system |
| `RevisedPrototype.py` | Earlier prototype version — menu structure and function stubs |
| `UMLandClassDiagrams.pdf` | Class diagram showing class relationships and design decisions |
| `library_items.txt` | Stored library item data |
| `members.txt` | Stored member data |
| `borrow_records.txt` | Stored borrowing transaction records |

## How to run

```bash
python "main(Final Group Code).py"
```

Follow the on-screen menu to select Staff or Member mode, then choose from the available options.

## Notes

This was a group project (Team 3) completed as part of a university programming course. Data is persisted between sessions using text file storage, with exception handling in place for file reading and writing.
