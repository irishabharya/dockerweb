# Website to run docker commands
## Prerequisites
* Install an httpd server on your Linux server.
* Copy the front.html and style.css file in ```/var/www/html```.
* Copy the back.py file in ```/var/www/cgi-bin```.
* Start the httpd services with ```systemctl start httpd```.
* As the server will be working with the privileges of Apache user there would be a few things you'll need to take care of:
* - In the ```/etc/groups``` folder add the apache group in your docker user by adding it after the third delimiter. The entry should look something like this: ```docker:x:973:apache```.
* - Stop SELinux by ```setenforce 0```.

And that's it you're good to go!
