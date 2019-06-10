# sample-symfony-setup
  run: yarn install inside the sample folder
  
  ### follow this steps:
  1. 	Go to: C:\Windows\System32\drivers\etc and open hosts file as administrator
  2. 	Add these lines to the file and name it as you wish:
	
	127.0.0.1 sample.local
	::1 sample.local
	
  3.	Open wamp and go to taskbar and click the wamp icon
  4.	After this click on Apache tab and open httpd-vhosts.conf
  5. 	Add these lines to the file:

    <VirtualHost *:80>
      ServerName sample.local
      ServerAlias sample.local
      DocumentRoot "path to the project location + \public"
      <Directory "path to the project location + \public">
        # enable the .htaccess rewrites
        AllowOverride All
        Require all granted
        </Directory>
    </VirtualHost>
   
   6.	After all this run:	composer require symfony/dotenv
