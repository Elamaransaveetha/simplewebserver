# EX01 Developing a Simple Webserver
## Date: 21/09/2023

## AIM:
To develop a simple webserver to serve html pages.

## DESIGN STEPS:
### Step 1: 
HTML content creation.

### Step 2:
Design of webserver workflow.

### Step 3:
Implementation using Python code.

### Step 4:
Serving the HTML pages.

### Step 5:
Testing the webserver.

## PROGRAM:
```

from http.server import HTTPServer, BaseHTTPRequestHandler
content = """

<!DOCTYPE html>
<html>
<head>
<title>ELAMARAN N's Webserver</title>
</head>

<body>
<h1>Top 5 revenue generating companies</h1>
<hr>
<h2>
<ol>
<li>Apple</li>
<li>Amazon</li>
<li>Microsoft</li>
<li>Infosys</li>
<li>Samsung</li>
</ol>
</h2>   

<h1>Done by ELAMARAN N(212222040041)

</body>
</html>

"""

class myhandler(BaseHTTPRequestHandler):
    def do_GET(self):
        print("request received")
        self.send_response(200)
        self.send_header('content-type', 'text/html; charset=utf-8')
        self.end_headers()
        self.wfile.write(content.encode())
server_address = ('',8001)
httpd = HTTPServer(server_address,myhandler)
print("my webserver is running...")
httpd.serve_forever()



```


## OUTPUT:
![2](https://github.com/Elamaransaveetha/simplewebserver/assets/119560403/f44f6383-fa3d-4fe8-ba50-5648b60d0d54)


![Screenshot 2023-10-21 090522](https://github.com/Elamaransaveetha/simplewebserver/assets/119560403/90932d47-f27c-4a61-81e2-be11be51b41c)


## RESULT:
The program for implementing simple webserver is executed successfully.
