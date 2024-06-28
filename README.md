# POSTHUB


It is a full-stack blog web application built with React on the frontend and Django/DRF on the backend integrated with AWS-S3 & AWS-RDS services.

<ins>Features:</ins>

- JWT authentication and authorization
- Responsive layout
- Users:
  - Users can:
    - Signup
    - Login
    - Logout
    - Update their email, password or profile picture
    - Delete their account
  - Currently loggedin user info is displayed on the home page
- Blog posts:
  - Users can:
    - Create a post
    - Edit their post
    - Delete their post
    - Applaud a post i.e. like/unlike a post
    - Comment on the post
    - Delete their comment
    - Save/unsave a post to their reading list
    - Save their draft and come back later to publish it
  - Category-wise blogs filtering on the home page
    - the categories supported are _arts, games, home, health, technology, recreation, business, society, sports, science_
  - Pagination of blogs
  - Search functionality i.e. search a blog by its title


- <ins>Users</ins>:

  - `api/users/user/signup/` - POST
  - `api/users/user/login/token/` - POST
  - `api/users/user/login/token/refresh/` - POST
  - `api/users/all/` - GET
  - `api/users/user/` - GET, PUT, DELETE

- <ins>Blogs</ins>:

  - `api/blogs/blogpost/` - POST
  - `api/blogs/all/` - GET
  - `api/blogs/blog/{blogId}/` - GET, PUT, DELETE
  - `api/blogs/userblogs/` - GET

- <ins>Comments</ins>:

  - `api/blogs/blog/{blogId}/commentpost/` - POST
  - `api/blogs/blog/{blogId}/comments/all/` - GET
  - `api/blogs/blog/{blogId}/comment/{commentId}/` - PUT, DELETE
  - `api/blogs/blog/{blogId}/totalcomments/` - GET

- <ins>Applauds</ins>:

  - `api/blogs/blog/{blogId}/applaud/` - POST
  - `api/blogs/blog/{blogId}/applauder/exists/` - GET

- <ins>Reading-list</ins>:
  - `api/blogs/blog/{blogId}/readinglist/save/` - POST
  - `api/blogs/readinglist/all/` - GET
  - `api/blogs/blog/{blogId}/reader/exists/` - GET


- Setup the project as per _General_ sub-section
- `cd backend`
- `py -m venv yourVenvName` - creates a virtual environment
- `yourVenvName\Scripts\activate.bat` - activates the virtual environment
- `pip install -r requirements.txt` - installs all modules
- `python manage.py makemigrations` & `python manage.py migrate` - migrates all the tables to db
- `python manage.py createsuperuser` - creates a superuser
- `python manage.py runserver` - runs the server

> NOTE: First run backend server (it will run on `http://127.0.0.1:8000`), then run frontend app (it will run on `http://127.0.0.1:3000`)


