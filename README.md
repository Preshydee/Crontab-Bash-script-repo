# Crontab-Bash-script-repo
Install ssmtp\
sudo apt-get install ssmtp

Access Config file\
sudo vim /etc/ssmtp/ssmtp.conf

Edit Config file\
mailhub=smtp.gmail.com:587\
useSTARTTLS=YES\
AuthUser=username-here\
AuthPass=password-here\
TLS_CA_File=/etc/pki/tls/certs/ca-bundle.crt\

Bash Script\
!/bin/sh\
SUBJECT="Test Subject"\
TO="adekoyapreciouspa@gmail.com"\
MESSAGE="Hey There! This is a test mail"\

echo $MESSAGE | sudo ssmtp -vvv $TO

#Permission to access file\
$ sudo chmod 755 scriptbash.sh 

#Run the app\
$ sudo ./scriptbash.sh

# Output\
[<-] 220 smtp.gmail.com ESMTP h8sm1096aae22880pfo.64 - gsmtp\
[->] EHLO kali\
[<-] 250 SMTPUTF8\
[->] STARTTLS\
[<-] 220 2.0.0 Ready to start TLS\
[->] EHLO kali\
[<-] 250 SMTPUTF8\
[->] AUTH LOGIN\
[<-] 334 VXNlcm5edhbAWU6\
[->] dmlzaGFsY2hhasd2dWhhbjIyMTJAZ21haWwuY29t\
[<-] 334 UGFzqc3dmvcmQ36\
[<-] 235 2.7.0 Accepted\
[->] MAIL FROM:<root@kali>
[<-] 250 2.1.0 OK h8smqer10962480pfo.64 - gsmtp\
[->] RCPT TO:<crazy@yopmail.com>\
[<-] 250 2.1.5 OK h8smqer10962480pfo.64 - gsmtp\
[->] DATA\
[<-] 354  Go ahead h8sm10962880pfo.64 - gsmtp\
[->] Received: by kali (sSMTP sendmail emulation); Thu, 19 Sep 2019 21:45:14 +0530\
[->] From: "root" <root@kali>\
[->] Date: Thu, 19 Sep 2019 21:45:14 +0530\
[->] Hey There! This is a test mail\
[->] 
[->] .
[<-] 250 2.0.0 OK  1568909725 h8smqer10962480pfo.64 - gsmtp
[->] QUIT
[<-] 221 2.0.0 closing connection h8smqer10962480pfo.64 - gsmtp
