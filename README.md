# Flask Blog with User Authentication

A full-stack blog web application built with **Flask**, featuring user authentication, post creation, and a commenting system. This project demonstrates practical use of Flask extensions, database relationships, and secure authentication patterns.

---

## Overview

This application allows users to register, log in, create blog posts, and leave comments on posts. Each post is linked to its author, and comments are associated with both the user and the post they belong to.

The project focuses on building a real-world backend structure using Flask, SQLAlchemy ORM, and secure password handling.

---

## Features

* User registration and login system
* Password hashing and salting using Werkzeug
* Authenticated users can create blog posts
* Comment system for logged-in users
* SQLAlchemy ORM relationships between Users, Posts, and Comments
* Form handling using Flask-WTF
* Bootstrap-styled forms with Bootstrap-Flask
* Flash messages for user feedback
* Secure session management with Flask-Login

---

## Tech Stack

Backend

* Python
* Flask
* Flask-Login
* Flask-WTF
* SQLAlchemy
* SQLite

Frontend

* HTML
* Jinja2 Templates
* Bootstrap 5

Security

* Werkzeug password hashing

---

## Project Structure

```
.
├── main.py
├── forms.py
├── posts.db
├── static
│   └── css
├── templates
│   ├── base.html
│   ├── index.html
│   ├── post.html
│   ├── login.html
│   ├── register.html
│   ├── make-post.html
│   └── header.html
```

---

## Database Models

### User

Represents registered users.

Fields:

* id
* email
* password (hashed)
* name

Relationships:

* One user can create many blog posts
* One user can write many comments

---

### BlogPost

Represents blog articles.

Fields:

* id
* title
* subtitle
* date
* body
* img_url
* author_id

Relationships:

* Each post belongs to one user
* One post can have many comments

---

### Comment

Represents comments left on posts.

Fields:

* id
* text
* author_id
* post_id

Relationships:

* Each comment belongs to one user
* Each comment belongs to one blog post

---

## Installation

Clone the repository

```
git clone https://github.com/ap-00007/Blog-capstone-2.git
cd flask-blog
```

Create a virtual environment

```
python -m venv venv
source venv/bin/activate
```

Install dependencies

```
pip install -r requirements.txt
```

Run the application

```
python main.py
```

Open in browser

```
http://127.0.0.1:5000
```

---

## Key Concepts Demonstrated

* Flask routing and view functions
* SQLAlchemy model relationships
* One-to-many database relationships
* Secure password storage
* Session-based authentication
* Form validation with Flask-WTF
* Template rendering with Jinja2
* Flash messaging for user feedback

---

## Future Improvements

* Rich text editor for posts
* User profile pages
* Admin dashboard
* Post editing and deletion
* Pagination for posts
* Image upload support
* REST API support
* Docker deployment

---

## License

This project is for educational purposes and can be freely modified and used.

---

## Author

Ashish Panda
Engineering Student | Learning Backend Development with Flask
