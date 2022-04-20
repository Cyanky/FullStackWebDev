## code in python  
```  
from flask import Flask

app = Flask(__name__)

@app.route('/')
def index():
    return 'Hello World!'  
    ```  
## in ubuntu  
```    
xjc@DESKTOP-S6I0E0I:~$ cd class-demos  // don't forget to cd the dictionary  

xjc@DESKTOP-S6I0E0I:~/class-demos$ FLASK_APP=flask-hello-app.py flask run  
 * Serving Flask app 'flask-hello-app.py' (lazy loading)
 * Environment: production
   WARNING: This is a development server. Do not use it in a production deployment.
   Use a production WSGI server instead.
 * Debug mode: off
 * Running on http://127.0.0.1:5000 (Press CTRL+C to quit)  
 ```
