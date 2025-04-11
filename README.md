# EX01 Developing a Simple Webserver
## Date:

## AIM:
To develop a simple webserver to serve html pages and display the list of protocols in TCP/IP Protocol Suite.

## DESIGN STEPS:
### Step 1: 
HTML content creation.

### Step 2:
Design of webserver workflow.

### Step 3:
Implementation using Python code.

### Step 4:
Import the necessary modules.

### Step 5:
Define a custom request handler.

### Step 6:
Start an HTTP server on a specific port.

### Step 7:
Run the Python script to serve web pages.

### Step 8:
Serve the HTML pages.

### Step 9:
Start the server script and check for errors.

### Step 10:
Open a browser and navigate to http://127.0.0.1:8000 (or the assigned port).

## PROGRAM:
```
<html>
    <head>
        <title>
            table tag
        </title>
       
    </head>
    <body>
        <center>
        <table border="3" align="center" cellpading="5" bgcolor="green">
            <tr bgcolor="yellow"><th bgcolor="red">S.no</th><th bgcolor="blue">Layer</th><th bgcolor="violet">protoclos</th></tr>
            <tr bgcolor="yellow"><td>1</td><td>Application Layer</td><td>Http,Ftp,ssh,Telnet</td></tr>
            <tr bgcolor="yellow"><td>2</td><td>Transport Layer</td><td>Tcp,Udp</td></tr>
            <tr bgcolor="yellow"><td>3</td><td>Internet Layer</td><td>IPv4,IPv6</td></tr>
            <tr bgcolor="yellow"><td>4</td><td>Network access layer</td><td>MAC</td></tr>
            <img src="c:\Users\admin\Desktop\logo.png" height="100" width="400"></img src>
            
                <h1 align="center">
                    <a href="https://lms2.saveetha.in/login/index.php">
                    Fundamental of web application</a>
                    <h2 align="center">LIST OF PROTOCOLS</h2>
    
                </h1>
            
        </table>
    </center>
    </body>
</html>
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
```
## OUTPUT:

![output](<Screenshot 2025-04-11 150715-1.png>)
## RESULT:
The program for implementing simple webserver is executed successfully.
