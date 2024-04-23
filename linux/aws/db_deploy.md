# EC2 Database Deploy

## Welcome to a guide on how to deploy your database to an EC2 instance.

### You should have already created the instance and the app deployment, with the database being next up! Please refer to the previous guides, if you have not yet done so.

## Guide
## 1. Commands
`#!/bin/bash`

## 2. config needrestart.config
## OR putting in noninteractive into the command which install things

echo updating... <br>
`sudo apt update -y` <br>
echo done!

## 3. Upgrade
echo upgrading... <br>
`sudo DEBIAN_FRONTEND=noninteractive apt upgrade -y`
echo done!

## 3. Install mongo db 7.0.6
### (initially, you could install the latest version of mongo db)
`sudo apt-get install gnupg curl
curl -fsSL https://www.mongodb.org/static/pgp/server-7.0.asc | \
   sudo gpg -o /usr/share/keyrings/mongodb-server-7.0.gpg \
   --dearmor
echo "deb [ arch=amd64,arm64 signed-by=/usr/share/keyrings/mongodb-server-7.0.gpg ] https://repo.mongodb.org/apt/ubuntu jammy/mongodb-org/7.0 multiverse" | sudo tee /etc/apt/sources.list.d/mongodb-org-7.0.list
sudo apt-get update
sudo apt-get install -y mongodb-org=7.0.6 mongodb-org-database=7.0.6 mongodb-org-server=7.0.6 mongodb-mongosh-shared-openssl3=2.2.4 mongodb-org-mongos=7.0.6 mongodb-org-tools=7.0.6`

## 4. Configure bind IP in mongo db config file - change it to 0.0.0.0
`sed -i "s,\\(^[[:blank:]]*bindIp:\\) .*,\\1 0.0.0.0," /etc/mongod.conf`

## 5. Restart mongo db (or start it if not already started)
`sudo systemctl start mongod`

## 6. Enable mongo db
`sudo systemctl enable mongod`
