# Python-for-Web-Development-How-to-Build-Dynamic-Websites-with-Python
Python for Web Development: How to Build Dynamic Websites with Python
This repository provides resources for building dynamic websites using Python. The materials cover essential web development concepts, including server-side scripting, database management, and front-end development.

Requirements

1. Python 3.x
2. Flask
3. SQLALCHEMY
4. Jinja2
5. HTML, CSS, and JavaScript

Installation

1. Clone this repository to your local machine
2. Install required packages using pip install -r requirements.txt
3. Start the server using python app.py
4. Navigate to http://localhost:5000 in your web browser

<h2>Usage</h2>

<b>1. Create your own Flask application by importing the necessary libraries and setting up a new Flask instance.</b>

<code>from flask import Flask, render_template

app = Flask(__name__)

@app.route('/')
def index():
    return render_template('index.html')</code>

<b>2. Add routes to your application to handle different URL requests.</b>

<code>@app.route('/about')
def about():
    return render_template('about.html')

@app.route('/contact')
def contact():
    return render_template('contact.html')</code>
    
  <b> 3.Create templates for each of your routes using Jinja2 syntax.</b>
  
  <code><!doctype html>
<html>
    <head>
        <title>Welcome to my website</title>
    </head>
    <body>
        <h1>Hello World!</h1>
        <p>This is the home page for my website.</p>
    </body>
</html> <code>

<b>4.Use SQLALCHEMY to manage your database and store data from user interactions.</b>

<code>from flask_sqlalchemy import SQLAlchemy
app.config['SQLALCHEMY_DATABASE_URI'] = 'sqlite:///mydatabase.db'
db = SQLAlchemy(app)
class User(db.Model):
    id = db.Column(db.Integer, primary_key=True)
    name = db.Column(db.String(50), nullable=False)
    email = db.Column(db.String(50), nullable=False)
    message = db.Column(db.String(200), nullable=False)
    def __repr__(self):
        return f'<User {self.name}>'<code>
        
  <b> 5. Use HTML, CSS, and JavaScript to style your website and create dynamic user interfaces. </b>
        
  <h2>Contributing</h2>
      
Contributions are welcome! Please open a pull request or file an issue if you find a bug or have a feature request.

lesson from <a href="https://www.igmguru.com/course/python-training/">Python Training</a>
