# EX01 Developing a Simple Webserver

# NAME:KIRUTHIGA.B

# REG.NO:212224040160

# Date:15.03.2025

# AIM:
To develop a simple webserver to serve html pages and display the configuration details of laptop.

# DESIGN STEPS:
## Step 1:
HTML content creation.

## Step 2:
Design of webserver workflow.

## Step 3:
Implementation using Python code.

## Step 4:
Serving the HTML pages.

## Step 5:
Testing the webserver.

# PROGRAM:
```
web.py

from http.server import HTTPServer, BaseHTTPRequestHandler
content = """
<html>
<title>Employee Details</title>
<body>
<table border="2" cellspacing="10"cellpadding"6">
<caption>Best Performer</caption>
<tr>
<th>emp.no</th>
<th>name</th>
<th>salary</th>
</tr>
<tr>
<th>100</th>
<th>balu</th>
<th>50000</th>
</tr>
<tr>
<th>101</th>
<th>mani</th>
<th>60000</th>
</tr>
<tr>
<th>102</th>
<th>priya</th>
<th>70000</th>
</tr>
<tr>
<th>103</th>
<th>shree</th>
<th>80000</th>
</tr>
<tr>
<th>104</th>
<th>siva</th>
<th>90000</th>
</tr>
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
server_address = ('',8000)
httpd = HTTPServer(server_address,myhandler)
print("my webserver is running...")
httpd.serve_forever()


urls.py

from django.contrib import admin
from django.urls import path

urlpatterns = [
    path('admin/', admin.site.urls),

]

```
# OUTPUT

![alt text](<Screenshot 2025-03-15 183844.png>) 


![alt text](<Screenshot 2025-03-15 183625.png>)


# RESULT:
The program for implementing simple webserver is executed successfully.
