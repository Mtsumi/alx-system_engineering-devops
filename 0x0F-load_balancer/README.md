# __Background Context__
In this project, I continued to build up the configuration of the web server issued in project 0x0B. I was issued two additional servers, one to replicate the Nginx configuration of my original server, and another to set up an HAproxy load balancer on to manage both web servers.
  * gc-[STUDENT_ID]-web-02-XXXXXXXXXX
  * gc-[STUDENT_ID]-lb-01-XXXXXXXXXX

This will allow us to be able to accept more traffic by doubling the number of web servers, and to make our infrastructure more reliable. If one web server fails, we will still have a second one to handle requests.

# __ Tasks __ 
### 0. Double the number of webservers

0-custom_http_response_header : Bash script that installs and configures Nginx on a server with a custom HTTP response header.
* The name of the HTTP header is X-Served-By.
* The value of the HTTP header is the hostname of the server.

### 1. Install your load balancer

1-install_load_balancer: Bash script that installs and configures HAproxy version 1.5 on a server.
* Enables management via the init script.
* Requests are distributed using a round-robin algorithm.