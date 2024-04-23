# EC2 App Deploy

## Welcome to a guide on how to deploy your app to an EC2 instance.

### You should have already created the EC2 instance via the previous guide, so this will be showcasing how to automate the procedure through the use of scripts.

## 1. Commands
`# !/bin/bash`

## 2. Update
echo updating... <br>
`sudo apt update -y` <br>
echo done!

## 3. Avoid user input and upgrade
echo upgrade packages... <br>
`sudo DEBIAN_FRONTEND=noninteractive apt upgrade -y` <br>
echo done!

## 4. Install nginx
echo installing nginx... <br>
`sudo DEBIAN_FRONTEND=noninteractive apt install nginx -y` <br>
echo done!

## C5. onfigure reverse proxy
echo configuring reverse proxy <br>
`sudo sed -i '50s/.*/\tproxy_pass http:\/\/54.78.147.108:3000;/' /etc/nginx/sites-enabled/default` <br>
echo done!

## 6. Restart nginx
echo restarting nginx...  <br>
`sudo systemctl restart nginx`  <br>
echo done!

## 7. Enable nginx
echo installing nginx...  <br>
`sudo systemctl enable nginx`  <br>
echo done!

## 8. Install js20
echo install js20  <br>
`curl -fsSL https://deb.nodesource.com/setup_20.x | sudo DEBIAN_FRONTEND=noninteractive -E bash - && sudo DEBIAN_FRONTEND=noninteractive apt-get install -y nodejs`  <br>
echo done

## 9. Check node version
echo check node js version  <br>
`node -v`  <br>
echo done!

## 10. Set DB_HOST env var
`export DB_HOST=mongodb://172.31.62.245:27017/posts`

## 11. Check DB_HOST env var
`printenv DB_HOST`

## 12. Clone app folder
echo getting app folder  <br>
`git clone https://github.com/Motala11/tech258_nodejs20_app.git`  <br>
echo got app folder

## 13. Going to app folder
echo going to app folder  <br>
`cd ~/tech258_nodejs20_app/app`  <br>
echo in app folder

## 14. Installing npm
echo installing npm  <br>
`sudo -E npm install`  <br>
echo installed npm

## 15. Installing pm2
echo installing pm2  <br>
`sudo npm install -g pm2` <br>
echo installed pm2

## 16. Stopping pm2
echo stopping pm2  <br>
`sudo pm2 stop all`  <br>
echo stopped pm2

## 17. Starting app
echo <br>
`pm2 start app.js app`  <br>
echo