1. Sign into AWS

2. Open EC2

3. Click Instances on Left Side

4. Click "Launch Instance"

5. Select "Amazon Linux AMI 2016.09.1 (HVM), SSD Volume Type"

6. Select Free Tier

7. Click review and launch

8. Press Launch

9. Create Pair

10. Download Pair

11. Launch Instance

12. Open list of Instances

13. Swap in your file name: ```chmod 400 ServerPair.pem```

14. Swap in your file name and ip address: ```ssh -i "ServerPair.pem" ec2-user@ec2-54-152-134-146.compute-1.amazonaws.com```

15. Update your instance ```sudo yum update -y```

16. Install Apache Web Server, MySQL, PHP ```sudo yum install -y httpd24 php70 mysql56-server php70-mysqlnd```

17. Start the Apache Web Server ```sudo service httpd start```

18. Make it so Apache Web Server runs on server boot: ```sudo chkconfig httpd on```

19. Verify it with: ```chkconfig --list httpd and httpd 0:off 1:off 2:on 3:on 4:on 5:on 6:off```

20. Go to your Public DNS or IPv4 Public IP: Example: ec2-54-152-134-146.compute-1.amazonaws.com

21. Create a new user group ```sudo groupadd www```

22. Add our EC2 User to this group ```sudo usermod -a -G www ec2-user```

23. Leave the current session exit

24. Sign back in. Swap in your file name and ip address: ```ssh -i "ServerPair.pem" ec2-user@ec2-54-152-134-146.compute-1.amazonaws.com```

25. Verify www exists by running: ```groups```

26. Give www permission on server files /var/www with ```sudo chown -R root:www /var/www```

27. Change file permissions: sudo chmod 2775 /var/www and ```find /var/www -type d -exec sudo chmod 2775 {} \;```

28. Add a index.html in var/www/html so touch /var/www/html/index.html and ```vi /var/www/html/index.html``` then add content.

29. Go back to Instances (like the list)

30. Right click on your new instance, select Networking, then Change Security Group

31. Take note of which one is selected

32. Open Security Groups on the left side: https://console.aws.amazon.com/ec2/

33. Edit the Inbound rules for that security group already assigned.

34. Add Rule and set the type to be HTTP

35. Files sit in ```ls -l /var/www```

36. Go to your IPv4 and you should see Hello World!

