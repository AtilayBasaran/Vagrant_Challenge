# Vagrant_Challenge
Preparing to run a flask application in vagrant managed virtualbox.

# Steps
1-Create simple Flask App
2-Vagrant download and virtual machine setup
3-Finally, to provide integration between the flask application and the virtual machine.

# How to run
1- Use vagrant up command from within vsc to run virtualbox. This will run virtualbox
2- Then install some vagrant command. This;
    vagrant ssh
    ls /var/www
    sudo apt update
    sudo apt install -y git
    git --version
    sudo apt install -y ansible
    ansible --version
    sudo apt install -y apache2
    ls /var/www
    ls /var/html
    exit
    After install this write last command --> vagrant reload
    localhost:1234 or 192.168.33.10
    vagrant ssh
    sudo nano /var/www/html/index.html
3- To run the flask application first open the command prompt
4- then run the commands set FLASK_APP=main:create_app and 
flask run respectively.