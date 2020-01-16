```sh
cd ~/.ssh/
```

GENERATE KEY PAIR:

`ssh-keygen -t rsa`

CONNECT TO VIRTUAL MACHINE:

`ssh -i ~/.ssh/id_rsa root@{IP}`

UPDATE PACKAGES TO BE ABLE TO INSTALL

`sudo apt-get update`


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

 `git clone https://github.com/miguelgimenezgimenez/productionWorkshop.git`



**Install dependencies and build client:**

`npm install && npm run build `



**FOREVER ( RUNS PROJECT DETACHED)**

`npm i -g forever`

`NODE_ENV=production forever start index.js` 



**NGINX**

INSTALL AND START NGINX 

`sudo apt-get install nginx`
`sudo service nginx start`

edit Nginx configuration

`sudo vi /etc/nginx/sites-available/default`

<u>inside nginx config file:</u>

```nginx
location / {
      proxy_pass http://127.0.0.1:5000/;
}

```


 `sudo service nginx reload`



