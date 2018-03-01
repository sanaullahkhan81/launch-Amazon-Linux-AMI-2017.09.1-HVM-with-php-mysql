Sign into AWS
Open EC2
Click Instances on Left Side
Click "Launch Instance"
Select "Amazon Linux AMI 2016.09.1 (HVM), SSD Volume Type"
Select Free Tier
Click review and launch
Press Launch
Create Pair
Download Pair
Launch Instance
Open list of Instances
Swap in your file name: chmod 400 ServerPair.pem
Swap in your file name and ip address: ssh -i "ServerPair.pem" ec2-user@ec2-54-152-134-146.compute-1.amazonaws.com
Update your instance sudo yum update -y
Install Apache Web Server, MySQL, PHP sudo yum install -y httpd24 php70 mysql56-server php70-mysqlnd
Start the Apache Web Server sudo service httpd start
Make it so Apache Web Server runs on server boot: sudo chkconfig httpd on
Verify it with: chkconfig --list httpd and httpd 0:off 1:off 2:on 3:on 4:on 5:on 6:off
Go to your Public DNS or IPv4 Public IP: Example: ec2-54-152-134-146.compute-1.amazonaws.com
Create a new user group sudo groupadd www
Add our EC2 User to this group sudo usermod -a -G www ec2-user
Leave the current session exit
Sign back in. Swap in your file name and ip address: ssh -i "ServerPair.pem" ec2-user@ec2-54-152-134-146.compute-1.amazonaws.com
Verify www exists by running: groups
Give www permission on server files /var/www with sudo chown -R root:www /var/www
Change file permissions: sudo chmod 2775 /var/www and find /var/www -type d -exec sudo chmod 2775 {} \;
Add a index.html in var/www/html so touch /var/www/html/index.html and vi /var/www/html/index.html then add content.
Go back to Instances (like the list)
Right click on your new instance, select Networking, then Change Security Group
Take note of which one is selected
Open Security Groups on the left side: https://console.aws.amazon.com/ec2/
Edit the Inbound rules for that security group already assigned.
Add Rule and set the type to be HTTP
Files sit in ls -l /var/www
Go to your IPv4 and you should see Hello World!

