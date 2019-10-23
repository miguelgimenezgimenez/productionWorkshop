

UPDATE PACKAGES TO BE ABLE TO INSTALL

`sudo apt-get update`

**NGINX**

INSTALL AND START NGINX 

`sudo apt-get install nginx`
`sudo service nginx start`

view Nginx configuration

`sudo vi /etc/nginx/sites-available/default`



**NODE**

INSTALL NODE

`sudo apt-get install nodejs npm`

SYMLINK NODE ( transform node command from nodejs=>node )

`sudo ln -s /usr/bin/nodejs /usr/bin/node`

INSTALL NVM:

`curl -o- https://raw.githubusercontent.com/creationix/nvm/v0.33.11/install.sh | bash`

install specific most recent version of node

`nvm install --lts`



**CLONE REPO**

`sudo mkdir -p /var/www`

 `git clone https://github.com/miguelgimenezgimenez/productionWorkshop.git

