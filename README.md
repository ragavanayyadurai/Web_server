# Developing a Simple Webserver
### Reference number:22008885
### Developed by:ragavendran
# AIM:

To develop a web server.

# DESIGN STEPS:

## Step 1:

HTML content creation is done

## Step 2:

Design of webserver workflow

## Step 3:

Implementation using Python code

## Step 4:

Serving the HTML pages.

## Step 5:

Testing the webserver

# PROGRAM:
```
from http.server import HTTPServer, BaseHTTPRequestHandler
content = """
<!DOCTYPE html>
<html>
<head>
<titlt>MY WEBSERVER</title>
</head>
<body>
<h1>WELCOME TO MY SIMPLE WEBSERVER</h1>
</body>
</html>
"""
class HelloHandler(BaseHTTPRequestHandler):
    def do_GET(self):
        print("request recieved")
        self.send_response(200)
        self.send_header('Content-type', 'text/html; charset=utf-8')
        self.end_headers()
        self.wfile.write(content.encode())


server_address = ('', 8080)
httpd = HTTPServer(server_address, HelloHandler)
print("my webserver is running.....")
httpd.serve_forever()

```

# OUTPUT:
![output](/output1.png)
![output](/output.png)
# RESULT:

The program is executed succesfully
