# Python Web Applications
This repo contains materials for the Python Web Applications Session 

[Top 10 Python Web Frameworks to Learn in 2018](https://hackernoon.com/top-10-python-web-frameworks-to-learn-in-2018-b2ebab969d1a)

# Flask on [sites.haverford](https://sites.haverford.edu/) or [digital.brynmawr](https://digital.brynmawr.edu/)
Is your app:
- [ ] simple
- [ ] performs one clear task
- [ ] pulls its data from an external source
- [ ] More a proof of concept than a production app 


Simple mad lib style paper title generator.  Based on most frequently occuring terms in the books and articles assigned for a class.  The script adds plausible title parts interspersed with terms from the list. 

```python
from flask import Flask, render_template, request, session, flash, redirect, url_for, g
import random
import csv
app = Flask(__name__)
application = app

@app.route('/')
def main():
    file_name = 'immigration_vocabulary.csv' 
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
```
[Instructions to deploy on sites.hc or digital.bmc](https://github.com/tri-co-hackathon-2019/python_web_applications/blob/master/Python%20at%20Reclaim%20Hosting.pdf)

# Django
Do you need:
- [ ] To manage data in a database or multiple types of databases
- [ ] Easy user accounts and user groups
- [ ] Need to keep data secure
- [ ] Needed for production

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
