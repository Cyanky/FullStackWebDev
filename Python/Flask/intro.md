HTTP and Flask Basics
17 minutos remaining


5 of 7 concepts completed
Introduction to Flask - Refresher
Google Chrome to look at different ways to ensure that the behavior is as you expectedReplay
Mute
Remaining Time -0:00
1xPlayback Rate
SubtitlesPicture-in-Picture

Fullscreen
Flask is the tool we'll use to create our API server.

It is a "micro" framework, which means that its core functionality is kept simple, but that there are numerous extensions to allow developers to add other functionality (such as authentication and database support).

In this section we will cover:

Creating a basic Flask application
Writing a basic endpoint
Checking the response using Curl.
Creating a basic Flask application
Lets return that, see it work again. Excellent.Replay
Mute
Remaining Time -0:00
1xPlayback Rate
SubtitlesPicture-in-Picture

Fullscreen
Set-Up Summary
Starting any Flask app will follow the same general flow for a simple application. The steps below are the same steps as taken in the screencast and can be referenced if you get stuck during the exercise.

Directory & Virtualenv Set Up
# Create the project directory and and navigate into it
mkdir FirstFlaskApp
cd FirstFlaskApp
# Create flaskr sub folder and create the __init__.py file into it
mkdir flaskr
touch __init__.py
Optional - It's your choice to work in a virtual environment. For this, you must have the virtualenv installed. Mac/Linux users can run:
# create and activate a virtual environment
python3 -m venv venv
source venv/bin/activate
Windows users can run:
> py -3 -m venv venv
> venv\Scripts\activate
Install flask using pip
Within the activated environment (if you've chosen so), use the following command to install Flask
pip3 install flask
Now, let's add some content to the __init__.py file. Then, you'll be ready to start working on your app!
Create the basic Flask app
Let's configure the basic Flask app in the /flaskr/__init__.py file.

# Import your dependencies
from flask import Flask, jsonify
# Define the create_app function
def create_app(test_config=None):
 # Create and configure the app
 # Include the first parameter: Here, __name__is the name of the current Python module.
 app = Flask(__name__)

 # Return the app instance
 return app
Up next, I'll include how to set up the application to handle specialized configuration.

First Endpoint with JSON
Before you return the app, use the @app.route decorator to create an endpoint to path / and define a function to handle that route.

@app.route('/')
def hello_world():
 return 'Hello, World!'
return app
Instead of returning text, use jsonify to send an object containing the message

return jsonify({'message':'Hello, World!'})
Run your application
In the command line, you'll run three lines of code. The first two lines tell the terminal where to find your application and to run it in development mode, which allows you to keep it running while it hotloads any modifications. The third actually starts the application. If running your application on Windows

# For Mac/Linux
export FLASK_APP=flaskr
export FLASK_ENV=development
# Make sure to run this command from the project directory (not from the flaskr)
flask run
For Windows cmd, use set instead of export:

> set FLASK_APP=flaskr
> set FLASK_ENV=development
> flask run
For Windows PowerShell, use $env:instead of export:

> $env:FLASK_APP = "flaskr"
> $env:FLASK_ENV = "development"
> flask run
After you start the application you'll see output like will look like the following:

* Serving Flask app "flaskr" (lazy loading)
* Environment: development
* Debug mode: on
* Running on http://127.0.0.1:5000/ (Press CTRL+C to quit)
* Restarting with stat
* Debugger is active!
* Debugger PIN: 192-247-084
Visit the provided URL and you should see {'message':'Hello, World!'} displayed. You can try adding more endpoints or changing the response before moving forward.

Add one more endpoint
 @app.route('/smiley')
 def smiley():
     return ':)'
As soon as you will save your code, the Flask server will automatically restart. Verify the output in the browser.
