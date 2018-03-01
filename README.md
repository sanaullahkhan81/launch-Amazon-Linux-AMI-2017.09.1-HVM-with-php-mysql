{\rtf1\ansi\ansicpg1252\cocoartf1561\cocoasubrtf200
{\fonttbl\f0\fswiss\fcharset0 Helvetica;\f1\fswiss\fcharset0 ArialMT;\f2\froman\fcharset0 Times-Roman;
}
{\colortbl;\red255\green255\blue255;\red27\green31\blue34;\red10\green77\blue204;\red0\green0\blue0;
}
{\*\expandedcolortbl;;\cssrgb\c14118\c16078\c18039;\cssrgb\c1176\c40000\c83922;\cssrgb\c0\c0\c0;
}
{\*\listtable{\list\listtemplateid1\listhybrid{\listlevel\levelnfc0\levelnfcn0\leveljc0\leveljcn0\levelfollow0\levelstartat1\levelspace360\levelindent0{\*\levelmarker \{decimal\}.}{\leveltext\leveltemplateid1\'02\'00.;}{\levelnumbers\'01;}\fi-360\li720\lin720 }{\listname ;}\listid1}}
{\*\listoverridetable{\listoverride\listid1\listoverridecount0\ls1}}
\paperw11900\paperh16840\margl1440\margr1440\vieww12600\viewh7800\viewkind0
\pard\tx566\tx1133\tx1700\tx2267\tx2834\tx3401\tx3968\tx4535\tx5102\tx5669\tx6236\tx6803\pardirnatural\partightenfactor0

\f0\fs24 \cf0 # launch-Amazon-Linux-AMI-2017.09.1-HVM-with-php-mysql\
\
\pard\tx220\tx720\pardeftab720\li720\fi-720\sl440\partightenfactor0
\ls1\ilvl0
\f1\fs32 \cf2 {\listtext	1.	}\expnd0\expndtw0\kerning0
\outl0\strokewidth0 \strokec2 Sign into AWS\uc0\u8232 \
\ls1\ilvl0\kerning1\expnd0\expndtw0 \outl0\strokewidth0 {\listtext	2.	}\expnd0\expndtw0\kerning0
\outl0\strokewidth0 \strokec2 Open EC2\uc0\u8232 \
\ls1\ilvl0\kerning1\expnd0\expndtw0 \outl0\strokewidth0 {\listtext	3.	}\expnd0\expndtw0\kerning0
\outl0\strokewidth0 \strokec2 Click Instances on Left Side\uc0\u8232 \
\ls1\ilvl0\kerning1\expnd0\expndtw0 \outl0\strokewidth0 {\listtext	4.	}\expnd0\expndtw0\kerning0
\outl0\strokewidth0 \strokec2 Click "Launch Instance"\uc0\u8232 \
\ls1\ilvl0\kerning1\expnd0\expndtw0 \outl0\strokewidth0 {\listtext	5.	}\expnd0\expndtw0\kerning0
\outl0\strokewidth0 \strokec2 Select "Amazon Linux AMI 2016.09.1 (HVM), SSD Volume Type"\uc0\u8232 \
\ls1\ilvl0\kerning1\expnd0\expndtw0 \outl0\strokewidth0 {\listtext	6.	}\expnd0\expndtw0\kerning0
\outl0\strokewidth0 \strokec2 Select Free Tier\uc0\u8232 \
\ls1\ilvl0\kerning1\expnd0\expndtw0 \outl0\strokewidth0 {\listtext	7.	}\expnd0\expndtw0\kerning0
\outl0\strokewidth0 \strokec2 Click review and launch\uc0\u8232 \
\ls1\ilvl0\kerning1\expnd0\expndtw0 \outl0\strokewidth0 {\listtext	8.	}\expnd0\expndtw0\kerning0
\outl0\strokewidth0 \strokec2 Press Launch\uc0\u8232 \
\ls1\ilvl0\kerning1\expnd0\expndtw0 \outl0\strokewidth0 {\listtext	9.	}\expnd0\expndtw0\kerning0
\outl0\strokewidth0 \strokec2 Create Pair\uc0\u8232 \
\ls1\ilvl0\kerning1\expnd0\expndtw0 \outl0\strokewidth0 {\listtext	10.	}\expnd0\expndtw0\kerning0
\outl0\strokewidth0 \strokec2 Download Pair\uc0\u8232 \
\ls1\ilvl0\kerning1\expnd0\expndtw0 \outl0\strokewidth0 {\listtext	11.	}\expnd0\expndtw0\kerning0
\outl0\strokewidth0 \strokec2 Launch Instance\uc0\u8232 \
\ls1\ilvl0\kerning1\expnd0\expndtw0 \outl0\strokewidth0 {\listtext	12.	}\expnd0\expndtw0\kerning0
\outl0\strokewidth0 \strokec2 Open list of Instances\uc0\u8232 \
\ls1\ilvl0\kerning1\expnd0\expndtw0 \outl0\strokewidth0 {\listtext	13.	}\expnd0\expndtw0\kerning0
\outl0\strokewidth0 \strokec2 Swap in your file name: 
\f2\fs26\fsmilli13333 chmod 400 ServerPair.pem
\f1\fs32 \uc0\u8232 \
\ls1\ilvl0\kerning1\expnd0\expndtw0 \outl0\strokewidth0 {\listtext	14.	}\expnd0\expndtw0\kerning0
\outl0\strokewidth0 \strokec2 Swap in your file name and ip address: 
\f2\fs26\fsmilli13333 ssh -i "ServerPair.pem" ec2-user@ec2-54-152-134-146.compute-1.amazonaws.com
\f1\fs32 \uc0\u8232 \
\ls1\ilvl0\kerning1\expnd0\expndtw0 \outl0\strokewidth0 {\listtext	15.	}\expnd0\expndtw0\kerning0
\outl0\strokewidth0 \strokec2 Update your instance 
\f2\fs26\fsmilli13333 sudo yum update -y
\f1\fs32 \uc0\u8232 \
\ls1\ilvl0\kerning1\expnd0\expndtw0 \outl0\strokewidth0 {\listtext	16.	}\expnd0\expndtw0\kerning0
\outl0\strokewidth0 \strokec2 Install Apache Web Server, MySQL, PHP 
\f2\fs26\fsmilli13333 sudo yum install -y httpd24 php70 mysql56-server php70-mysqlnd
\f1\fs32 \uc0\u8232 \
\ls1\ilvl0\kerning1\expnd0\expndtw0 \outl0\strokewidth0 {\listtext	17.	}\expnd0\expndtw0\kerning0
\outl0\strokewidth0 \strokec2 Start the Apache Web Server 
\f2\fs26\fsmilli13333 sudo service httpd start
\f1\fs32 \uc0\u8232 \
\ls1\ilvl0\kerning1\expnd0\expndtw0 \outl0\strokewidth0 {\listtext	18.	}\expnd0\expndtw0\kerning0
\outl0\strokewidth0 \strokec2 Make it so Apache Web Server runs on server boot: 
\f2\fs26\fsmilli13333 sudo chkconfig httpd on
\f1\fs32 \uc0\u8232 \
\ls1\ilvl0\kerning1\expnd0\expndtw0 \outl0\strokewidth0 {\listtext	19.	}\expnd0\expndtw0\kerning0
\outl0\strokewidth0 \strokec2 Verify it with: 
\f2\fs26\fsmilli13333 chkconfig --list httpd
\f1\fs32  and 
\f2\fs26\fsmilli13333 httpd 0:off 1:off 2:on 3:on 4:on 5:on 6:off
\f1\fs32 \uc0\u8232 \
\ls1\ilvl0\kerning1\expnd0\expndtw0 \outl0\strokewidth0 {\listtext	20.	}\expnd0\expndtw0\kerning0
\outl0\strokewidth0 \strokec2 Go to your Public DNS or IPv4 Public IP: Example: ec2-54-152-134-146.compute-1.amazonaws.com\uc0\u8232 \
\ls1\ilvl0\kerning1\expnd0\expndtw0 \outl0\strokewidth0 {\listtext	21.	}\expnd0\expndtw0\kerning0
\outl0\strokewidth0 \strokec2 Create a new user group 
\f2\fs26\fsmilli13333 sudo groupadd www
\f1\fs32 \uc0\u8232 \
\ls1\ilvl0\kerning1\expnd0\expndtw0 \outl0\strokewidth0 {\listtext	22.	}\expnd0\expndtw0\kerning0
\outl0\strokewidth0 \strokec2 Add our EC2 User to this group 
\f2\fs26\fsmilli13333 sudo usermod -a -G www ec2-user
\f1\fs32 \uc0\u8232 \
\ls1\ilvl0\kerning1\expnd0\expndtw0 \outl0\strokewidth0 {\listtext	23.	}\expnd0\expndtw0\kerning0
\outl0\strokewidth0 \strokec2 Leave the current session 
\f2\fs26\fsmilli13333 exit
\f1\fs32 \uc0\u8232 \
\ls1\ilvl0\kerning1\expnd0\expndtw0 \outl0\strokewidth0 {\listtext	24.	}\expnd0\expndtw0\kerning0
\outl0\strokewidth0 \strokec2 Sign back in. Swap in your file name and ip address: 
\f2\fs26\fsmilli13333 ssh -i "ServerPair.pem" ec2-user@ec2-54-152-134-146.compute-1.amazonaws.com
\f1\fs32 \uc0\u8232 \
\ls1\ilvl0\kerning1\expnd0\expndtw0 \outl0\strokewidth0 {\listtext	25.	}\expnd0\expndtw0\kerning0
\outl0\strokewidth0 \strokec2 Verify 
\f2\fs26\fsmilli13333 www
\f1\fs32  exists by running: 
\f2\fs26\fsmilli13333 groups
\f1\fs32 \uc0\u8232 \
\ls1\ilvl0\kerning1\expnd0\expndtw0 \outl0\strokewidth0 {\listtext	26.	}\expnd0\expndtw0\kerning0
\outl0\strokewidth0 \strokec2 Give 
\f2\fs26\fsmilli13333 www
\f1\fs32  permission on server files 
\f2\fs26\fsmilli13333 /var/www
\f1\fs32  with 
\f2\fs26\fsmilli13333 sudo chown -R root:www /var/www
\f1\fs32 \uc0\u8232 \
\ls1\ilvl0\kerning1\expnd0\expndtw0 \outl0\strokewidth0 {\listtext	27.	}\expnd0\expndtw0\kerning0
\outl0\strokewidth0 \strokec2 Change file permissions: 
\f2\fs26\fsmilli13333 sudo chmod 2775 /var/www
\f1\fs32  and 
\f2\fs26\fsmilli13333 find /var/www -type d -exec sudo chmod 2775 \{\} \\;
\f1\fs32 \uc0\u8232 \
\ls1\ilvl0\kerning1\expnd0\expndtw0 \outl0\strokewidth0 {\listtext	28.	}\expnd0\expndtw0\kerning0
\outl0\strokewidth0 \strokec2 Add a 
\f2\fs26\fsmilli13333 index.html
\f1\fs32  in 
\f2\fs26\fsmilli13333 var/www/html
\f1\fs32  so 
\f2\fs26\fsmilli13333 touch /var/www/html/index.html
\f1\fs32  and 
\f2\fs26\fsmilli13333 vi /var/www/html/index.html
\f1\fs32  then add content.\uc0\u8232 \
\ls1\ilvl0\kerning1\expnd0\expndtw0 \outl0\strokewidth0 {\listtext	29.	}\expnd0\expndtw0\kerning0
\outl0\strokewidth0 \strokec2 Go back to Instances (like the list)\uc0\u8232 \
\ls1\ilvl0\kerning1\expnd0\expndtw0 \outl0\strokewidth0 {\listtext	30.	}\expnd0\expndtw0\kerning0
\outl0\strokewidth0 \strokec2 Right click on your new instance, select 
\f2\fs26\fsmilli13333 Networking
\f1\fs32 , then 
\f2\fs26\fsmilli13333 Change Security Group
\f1\fs32 \uc0\u8232 \
\ls1\ilvl0\kerning1\expnd0\expndtw0 \outl0\strokewidth0 {\listtext	31.	}\expnd0\expndtw0\kerning0
\outl0\strokewidth0 \strokec2 Take note of which one is selected\uc0\u8232 \
\ls1\ilvl0\kerning1\expnd0\expndtw0 \outl0\strokewidth0 {\listtext	32.	}\expnd0\expndtw0\kerning0
\outl0\strokewidth0 \strokec2 Open Security Groups on the left side: {\field{\*\fldinst{HYPERLINK "https://console.aws.amazon.com/ec2/"}}{\fldrslt \cf3 \ul \ulc3 \strokec3 https://console.aws.amazon.com/ec2/}}\uc0\u8232 \
\ls1\ilvl0\kerning1\expnd0\expndtw0 \outl0\strokewidth0 {\listtext	33.	}\expnd0\expndtw0\kerning0
\outl0\strokewidth0 \strokec2 Edit the Inbound rules for that security group already assigned.\uc0\u8232 \
\ls1\ilvl0\kerning1\expnd0\expndtw0 \outl0\strokewidth0 {\listtext	34.	}\expnd0\expndtw0\kerning0
\outl0\strokewidth0 \strokec2 Add Rule and set the type to be 
\f2\fs26\fsmilli13333 HTTP
\f1\fs32 \uc0\u8232 \
\ls1\ilvl0\kerning1\expnd0\expndtw0 \outl0\strokewidth0 {\listtext	35.	}\expnd0\expndtw0\kerning0
\outl0\strokewidth0 \strokec2 Files sit in 
\f2\fs26\fsmilli13333 ls -l /var/www
\f1\fs32 \uc0\u8232 \
\ls1\ilvl0\kerning1\expnd0\expndtw0 \outl0\strokewidth0 {\listtext	36.	}\expnd0\expndtw0\kerning0
\outl0\strokewidth0 \strokec2 Go to your IPv4 and you should see 
\f2\fs26\fsmilli13333 Hello World!
\f1\fs32 \uc0\u8232 \
\pard\pardeftab720\sl280\partightenfactor0

\f2\fs24 \cf4 \strokec4 \
\pard\tx566\tx1133\tx1700\tx2267\tx2834\tx3401\tx3968\tx4535\tx5102\tx5669\tx6236\tx6803\pardirnatural\partightenfactor0

\f0 \cf0 \kerning1\expnd0\expndtw0 \outl0\strokewidth0 \
}