## This is a step by step guide to set up a Flask app on sites.haverford.edu or digital.brynmawr.edu  

### Section I Make the App

1) Here's a very simple "Hello World" app from the [Flask documentation.](http://flask.pocoo.org/).  In Mac or Linux, just type `cat > app.py` and paste the following into the file: 
```Python
from flask import Flask
app = Flask(__name__)
application = app

@app.route("/")
def hello():
    return "Hello World!"
 ```  
 You can now run the app:
 ```
$ pip install Flask
$ FLASK_APP=app.py flask run
 * Running on http://localhost:5000/
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

4) Click on Setup Python App.  You'll see a section titled "Setup new application."  Choose your prefered version of Python, enter a name for the app directory and then enter an App Domain/URI where the app can be accessed from the web.  Then click Setup. 

5) Next we need to insall Flask.  In modules, enter "flask" and the version you'd like to use. Click add and then update. You should see that it's installed all the dependencies needed for Flask 
- Click	7.0	[x]
- Flask	1.0.2	[x]
- itsdangerous	1.1.0	[x]
- Jinja2	2.10	[x]
- MarkupSafe	1.1.0	[x]
- Werkzeug	0.14.1	[x]
- wheel	0.29.0	[x]

6) Now move to the File Manager.  There should now be a folder with the name that you entered in step 4 with public and tmp subdirectories. 

7) Select the public directory and then upload file.  You can now upload your app.py file from Section I. Note the path for the next step. For example: `Select the file you want to upload to “/home/ajancosi/testing/public”.`

8) Now go back to Setup Python App.  Click on `WGI file location` and click Edit.  Here you enter the path to your file, the filename and :application.  So my file location will be `/home/ajancosi/testing/public` (from step 7), plus `app.py` (from section I step 1), and then `:application`.  Together I get `/home/ajancosi/testing/public/app.py:application`. Now click Save and Update. 

