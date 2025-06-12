## This Readme shall explain the steps I took to acheive the project (Server setup, web server, and deployment)

### Server Setup
- I used AWS for this project. Created a new EC2 instance which I titled "MY Web Server". I allowed inbound traffic into port 22 (SSH), port 80 (http) and port 443 (https)
- Next, I SSh into the server from my VScode terminal having already created a Key Pair.
- Inside the terminal I created a folder which I called "second_semester_exam".

### Web Server Setup
- Next is setting up a web server, I chose Nginx.
- I ran the following codes to install Nginx on the machine

    1. sudo apt update
    2. sudo apt install nginx
    3. sudo systemctl start nginx
    4. sudo systemctl enable nginx
    5. sudo systemctl status nginx
- I opened a web browser and enter my server’s IP address. I saw the default Nginx welcome page which confirmed that installation and configuration work well.

### Deployment
