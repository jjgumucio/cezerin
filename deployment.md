## Deployment on VM

- Install NVM: ```curl -o- https://raw.githubusercontent.com/creationix/nvm/v0.33.11/install.sh | bash``` [NVM Repo](https://github.com/creationix/nvm)
- Install Node: ```nvm install <latest LTS version>``` (To see available versions use ```nvm ls-remote```)
- Install MongoDB: Vía distro package manager i.e. ```apt-get install mongodb```
- Install PM2: ```npm install pm2 -g```
- Install git: Vía distro package manager i.e. ```apt-get install git-core```
- Clone the repo: ```git clone https://github.com/utipsDevelopers/ucommerce.git```
- Change directory to the project: ```cd ucommerce```
- Install dependencies: ```npm install```
- Run: ```pm2 start process.json```
