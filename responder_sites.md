This is how to create a responder app in sites.hc or digital.bmc
`conda create -n responder python=3.7`  
`pip install responder`  

```python
import responder

api = responder.API()

@api.route("/")
async def hello(req, resp):
    resp.text = "hello, world!"

if __name__ == "__main__":
    api.run()```
    
To template:  
```python
@api.route("/hello/{who}/html")
def hello_html(req, resp, *, who):
    resp.content = api.template('hello.html', who=who)
    ```
