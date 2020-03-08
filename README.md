# Task List Web Application
## A simple Flask web application with CRUD database functionality
### Reference https://github.com/jakerieger/FlaskIntroduction

---
## Create the database 
```bash
$python
```
```python
>>from app import db
>>db.create_all() 
```
Reference https://flask-sqlalchemy.palletsprojects.com/en/2.x/quickstart/  

---
## Starting and stopping the web app
```bash
$python app.py
```
Then open http://127.0.0.1:5000/ in your web browser.
Press CTRL+C to quit.

---
## Changes to the original reference code
Add "required" attribute to the HTML create and update POST forms
```html
<div class="form">
    <form action="/" method="POST">
        <input type="text" name="content" id="content" required>
        <input type="submit" value="Add Task">
    </form>
</div>
```
Reference: https://stackoverflow.com/questions/9844150/flask-sqlalchemy-nullable-false/9845764  
  
---
## Fix on VS Code linting errors on flask_sqlalchemy SQLAlchemy member functions
Add to VS Code settings
```
"python.linting.pylintArgs": ["--load-plugins", "pylint_flask"]
```
Reference https://stackoverflow.com/questions/53975234/instance-of-sqlalchemy-has-no-column-member  