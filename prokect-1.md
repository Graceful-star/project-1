## Documentation of Project1
### Step 1

a. install sudo apache

`sudo apt update`

![install sudo apt](image/apt-update1.png)
	Apache2 package installation
    `sudo apt install apache2`
    ![Install apache](image/install-apache2.png)
    b. I verified that apache2 is running as a service in my OS
    `sudo systemctl status apache2`
    	![Verify apache](image/apache-verification.png)
    c. I accessed my server locally in my ubuntu shell
    `
 curl http://localhost:80`
 	![Access server](image/curl-command.png)
     	![Access server](image/curl-command12.png)

  ### Step 2
  a. I installed mysql server
  	`sudo apt install mysql-server`
      	![Install mysql](image/install-mysql.png)
  b. I ran a security script
     `sudo mysql_secure_installation`
     
     ![Secure installation](image/secure-installation.png)
     ![Secure installation](image/secure-installation2.png)
  c. I validated my password login
  d. I checked if I'm able to login to mysql console
     `sudo mysql`
     ![Sudo mysql](image/sudo-mysql.png)
  e. I exit the mysql console
     `mysql> exit`
     ![Exit mysql](image/mysql-exit.png)

### Step 3
a. I installed the three packages at once
    `sudo apt install php libapache2-mod-php php-mysql`
    ![Install php](image/install-php.png)
b. I ran this command to confirm the php version
    `php -v`
    ![Exit mysql](image/php-version.png)

### Step 4
a. I created directory for projectlamp using mkdir
   `sudo mkdir /var/www/projectlamp`
   ![Create directory](image/mkdir.png)
b. I assigned ownership of the directory
     `sudo chown -R $USER:$USER /var/www/projectlamp`
      ![sudo chown](image/ownership-directory.png)

c. I created a new configuration file in Apache's directory
   `sudo vi /etc/apache2/sites-available/projectlamp.conf`
    ![Sudo site](image/site-availability.png)
d. I used a2ensite command to enable the virtual host
    `sudo a2ensite projectlamp`
e. I ensured my configuration file doesn't contain syntax error
     `sudo apache2ctl configtest`
     ![Configuration test](image/configest.png)
f. I reloaded apache
`sudo systemctl reload apache2`
![Configuration test](image/reload-apache.png)

### Step 5
a. I edited the configuration file and changed the order at which it was listed
    `sudo vim /etc/apache2/mods-enabled/dir.conf`
    ![Sudo vim](image/editing.png)
    ![Sudo vim](image/sudo-vim.png)
b. I reloaded apache for the changes to take effect
       `sudo systemctl reload apache2`
    ![Reload apache](image/system-reload.png)
c. I created a new file in my custom root web user
    `vim /var/www/projectlamp/index.php`
    ![Index](image/new-vim.png)
d. I saved and closed the file, then I refreshed the page
     ![PHP](image/php-server.png)
e. I removed the file after checking it on the site
    `sudo rm /var/www/projectlamp/index.php`
    ![Sudo removal](image/removal.png)










   




     	

        
