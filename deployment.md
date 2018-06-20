## Deployment on Ubuntu 16 VM
- Install NVM: ```curl -o- https://raw.githubusercontent.com/creationix/nvm/v0.33.11/install.sh | bash``` [NVM Repo](https://github.com/creationix/nvm)
- Install Node: ```nvm install <latest LTS version>``` (To see available versions use ```nvm ls-remote```)
- Install MongoDB: (Default Mongo version from package managers are old: [Source](https://docs.mongodb.com/manual/tutorial/install-mongodb-on-ubuntu/))
  - Import the public key used by the package management system: ```sudo apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv 2930ADAE8CAF5059EE73BB4B58712A2291FA4AD5```
  - Create a list file for MongoDB: ```echo "deb [ arch=amd64,arm64 ] https://repo.mongodb.org/apt/ubuntu xenial/mongodb-org/3.6 multiverse" | sudo tee /etc/apt/sources.list.d/mongodb-org-3.6.list```
  - Reload local package database: ```apt-get update```
  - Install the latest stable version of MongoDB: ```sudo apt-get install -y mongodb-org```
- Install PM2: ```npm install pm2 -g```
- Install git: Vía distro package manager i.e. ```apt-get install git-core```
- Clone the repo: ```git clone https://github.com/utipsDevelopers/ucommerce.git```
- Change directory to the project: ```cd ucommerce```
- Install dependencies: ```npm install```
- Follow instruction on Cezerins project: [Cezerin Repo](https://github.com/cezerin/cezerin/blob/master/docs/getting-started.md)
- Set up NGINX:
  - Install NGINX: ```apt-get install nginx```
  - [Instructions to install](https://www.digitalocean.com/community/tutorials/how-to-install-nginx-on-ubuntu-18-04)
  - [Instructions to config](https://www.digitalocean.com/community/tutorials/how-to-set-up-a-node-js-application-for-production-on-ubuntu-16-04)