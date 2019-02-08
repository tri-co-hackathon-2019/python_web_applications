# Python Web Applications
This repo contains materials for the Python Web Applications Session 

[Top 10 Python Web Frameworks to Learn in 2018](https://hackernoon.com/top-10-python-web-frameworks-to-learn-in-2018-b2ebab969d1a)

# Flask on sites.haverford or digital.brynmawr
```python
from flask import Flask, render_template, request, session, flash, redirect, url_for, g
import random
import csv

#DATABASE = 'immigration_vocabulary.csv' #configuration
app = Flask(__name__)
application = app

#app.config.from_object(__name__) # pulls in configurations by looking for UPPERCASE variables

#def connect_csv():
#    return csv.connect(app.config['DATABASE'])

@app.route('/')
def main():
    file_name = 'immigration_vocabulary.csv' #this needs to be set to the current path
    dict_list = []

    with open(file_name, 'rb') as fd:
        reader = csv.DictReader(fd)
        for line in reader:
            dict_list.append(line)        
        
    ands = ['Through','Beyond','Eternal','When','Explorations of','The Origins of','The Future of'] 
    ors = ['and','or','without', 'since','under the','with']
    discp = ['A Hisory of','Gender and','The Political Economy of','A Discourse on','The Politics of','Outline of a Theory of']
    word1 = random.choice(dict_list)
    word2 = random.choice(dict_list)
    ands1 = random.choice(ands)
    disp1 = random.choice(discp)
    ors1 = random.choice(ors)
    word3 = random.choice(dict_list)


    choice = ' '+ands1+' '+ word1['Word']+' '+ors1+' '+word2['Word']+' - '+disp1+' '+ word3['Word']
    print choice
    return render_template('main.html', choice=choice)

if __name__ == '__main__':
    app.run(debug=True)```
    
# Django
* [Mozilla Django Tutorial](https://developer.mozilla.org/en-US/docs/Learn/Server-side/Django)
* [Real Python Django Tutorials](https://realpython.com/tutorials/django/)  
* [Django Girls](https://djangogirls.org/) 
* [Haverford College Django Cookbook](https://github.com/HCDigitalScholarship/ds-cookbook)    
* [Example App 90-Sourcebook](https://slavicdh.apjan.co/)  

* Simple content management, [Django flatpages](https://github.com/HCDigitalScholarship/ds-cookbook/tree/master/django_flatpages)
* For spatial data, [GeoDjango](https://github.com/HCDigitalScholarship/ds-cookbook/tree/master/GeoDjango%20and%20Geocoding)
* [Multi-lingual applications](https://github.com/HCDigitalScholarship/ds-cookbook/tree/master/internationalization)
* [Simple Machine Learning APIs](https://github.com/HCDigitalScholarship/ds-cookbook/tree/master/google_vision)
* [Autocomplete fields for forms](https://github.com/HCDigitalScholarship/ds-cookbook/tree/master/django-autocomplete)
* Powerful spreadsheets and tables, [jQuery DataTables](https://github.com/HCDigitalScholarship/ds-cookbook/tree/master/datatables-server-side-processing)
* [Easy image grid](https://codepen.io/Vestride/pen/ZVWmMX)
