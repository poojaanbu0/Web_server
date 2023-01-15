# Developing a Simple Webserver

# AIM:
To develop a simple webserver to serve html pages


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
<html>
<head>
</head>
<body>
<h1>Welcome</h1>
</body>
</html>
"""
class HelloHandler(BaseHTTPRequestHandler):
    def do_GET(self):
        print("request received")
        self.send_response(200)
        self.send_header('Content-type', 'text/html; charset=utf-8')
        self.end_headers()
        self.wfile.write(content.encode())
server_address = ('', 80)
httpd = HTTPServer(server_address, HelloHandler)
print("my webserver is running....")
httpd.serve_forever()
```

# OUTPUT:
![](./ex01code.png)
![output](./ex01.jpeg)

# RESULT:

The program for implementing Simple Web Server has been executed succesfully.
