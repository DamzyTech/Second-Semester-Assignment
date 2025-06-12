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
- I opened a web browser and enter my server’s IP address (http://18.130.178.12/). I saw the default Nginx welcome page which confirmed that installation and configuration work well.

### Deployment
- I created an index.html file on my local machine. In the file I created a landing page for an AI healthtech startup compnay called "Wellness". I added a few extra features like a nav bar, footer, and social media links. I styled the webpage using CSS and Tailwind CSS to make it more beautiful. I added a section where I spoke about myself, my experience and expertise.
- I initialized git, created an SSH key which I used to connect with my github account.
- I created a github repository and then pushed the index.html file from my local machine to the github repo using the following commands
    1. git init
    2. git status
    3. git add .
    4. git commit
    5. git push origin master
- I logged into my AWS linux server, I cloned the repository (Having done SSH connections)
- Now I have the index.html on my AWS linux server.
- I now copied the index.html file to the nginx default index.html to replace it. I used the command
        "sudo cp index.html /var/www/html/"
- I entered my server's IP address (http://18.130.178.12/), and it displayed the content below:
  <img width="947" alt="image" src="https://github.com/user-attachments/assets/12974cfc-4a63-4967-b2a7-32c5422ea014" />
