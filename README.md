# Internship_Task1
 Library Management System - Database 

This project defines a normalized SQL Server database schema for managing a library's operations, including books, categories, members, authors, librarians, and book borrowing transactions.

 Database Overview

The schema supports:

- Book and category management
- Author tracking with many-to-many relationships
- Member registration and activity
- Librarian records
- Borrowing and return of books, with fine and return tracking

Tables Summary

Categories:
	Stores book categories along with audit fields like Created_by, Updateddate, and Is_active.

Books:
	Contains metadata about books such as title, publisher, year, and ISBN. Each book is linked to a category.

Authors:
	Stores details about authors, including name and an optional biography.

BookAuthors:
	Manages the many-to-many relationship between books and authors.

Members:
	Holds records of library members, including their name, email, phone number, and join date.

Librarians:
	Maintains information about library staff who handle book borrowing and returns.

Borrowed_Books:
	Tracks which books are issued to which members, by which librarian, including issue date, return date, actual return date, fine amount, and return status.

Features

- Audit tracking: Created_by, Updatedby, Createddate, Updateddate
- Soft delete support via Is_active fields
- Data integrity through FOREIGN KEY constraints
- Uniqueness constraints on ISBN and email fields
- Support for multiple authors per book

