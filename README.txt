### 1. server 

===> cd to folder server

cd /home/user/Desktop/dashboard/server/server/api

===> install packages

source server.sh

===> run 

sudo kill -9 $(sudo lsof -t -i:5001) 

export FLASK_APP=api

export FLASK_ENV=development

flask run --port 5001 --host 0.0.0.0 


### 2. excel_api

===> cd to folder excel_api

cd /home/user/Desktop/dashboard/excel_api

===> install packages

source excel_api.sh

===> create database

sudo mysql < data/mySQL/script.sql

sudo mysql < data/mySQL/script_2.sql

sudo mysql 

	///copy and paste to mysql>

	  ALTER USER 'root'@'localhost' IDENTIFIED WITH mysql_native_password BY '1234';

	  FLUSH PRIVILEGES;

	  EXIT

===> edit file .py

cd /home/user/Desktop/dashboard/excel_api

sudo nano lib.py

	///edit :

		  app.config['MYSQL_USER'] = 'root'
		  
		  app.config['MYSQL_PASSWORD'] = '1234'


===> run 

sudo kill -9 $(sudo lsof -t -i:5000)

export FLASK_APP=flask_app

export FLASK_ENV=development

flask run --port 5000 --host 0.0.0.0 


### 3. sku_dashboard-develop

===> install nodejs  npm    yarn

source sku.sh

exit

===>  run : must open new terminal 

cd /home/user/Desktop/dashboard/sku-dashboard-develop/enviroments

yarn install

yarn start 

===> config ip 

cd /home/user/Desktop/dashboard/sku-dashboard-develop/src

sudo nano route.js 

	/// edit ip ---> CTRL + O + ENTER + CTRL X


cd /home/user/Desktop/dashboard/sku-dashboard-develop/enviroments

sudo nano .env.development
	
	/// edit ip ---> CTRL + O + ENTER + CTRL X


### 4. log-in 

user : KAM_Lazada

pass : KAM_Lazada@
