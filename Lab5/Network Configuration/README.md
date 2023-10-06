Practical part 

Make a web server out of the virtual machine and install the following components 

Apache 
PHP 
MySQL 
phpMyAdmin 

as a result, you must connect through the browser of the host machine to the web server 

------------------------------------------------------------------------------------------------------------------------------------------

To complete the practical part of this exercise, you will need to:

1. Install Apache, PHP, MySQL, and phpMyAdmin on the virtual machine.
2. Configure the web server so that it is accessible from the host machine.
3. Connect to the web server through the browser of the host machine.

Here are the steps in more detail:

**1. Install Apache, PHP, MySQL, and phpMyAdmin on the virtual machine.**

On Fedora, you can install these packages using the following commands:

```
sudo dnf install httpd php mysql phpmyadmin
```

**2. Configure the web server so that it is accessible from the host machine.**

By default, the web server on Fedora is only accessible from the virtual machine itself. To make it accessible from the host machine, you need to edit the firewall configuration.

Open the firewall configuration file:

```
sudo nano /etc/firewalld/zones/public.xml
```

Add the following line to the file:

```
<service name="http" />
```

Save and close the file.

Reload the firewall configuration:

```
sudo firewall-cmd reload
```

**3. Connect to the web server through the browser of the host machine.**

Open a web browser on the host machine and enter the IP address of the virtual machine in the address bar. You should see the default Apache welcome page.

If you have installed phpMyAdmin, you can access it by going to the following URL:

```
http://<ip address of virtual machine>/phpmyadmin
```

You should be able to log in to phpMyAdmin using the default username and password (`root` and `password`).

Congratulations! You have now successfully configured a web server on the virtual machine and made it accessible from the host machine.
