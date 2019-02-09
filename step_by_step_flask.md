## This is a step by step guide to set up a Flask app on sites.haverford.edu or digital.brynmawr.edu  

### Section I Make the App

1) Here's a very simple "Hello World" app from the [Flask documentation.](http://flask.pocoo.org/)  
```Python
from flask import Flask
app = Flask(__name__)

@app.route("/")
def hello():
    return "Hello World!"
 ```  
 
### Section II Deploy your App on sites.HC or digital.BMC
1) Log in to [sites.haverford.edu](https://sites.haverford.edu/) or [digital.brynmawr.edu](https://digital.brynmawr.edu/)
2) Click on Dashboard 
3) In this tutorial we'll be using:  

![alt text](https://raw.githubusercontent.com/tri-co-hackathon-2019/python_web_applications/master/Screen%20Shot%202019-02-08%20at%209.24.40%20PM.png
 "File manager image")
* File Manager in the Files section   


![alt text](https://raw.githubusercontent.com/tri-co-hackathon-2019/python_web_applications/master/Screen%20Shot%202019-02-08%20at%209.24.52%20PM.png
 "Python apps image")
* Setup Python App in the Software section 


