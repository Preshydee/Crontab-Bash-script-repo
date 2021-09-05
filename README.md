# Crontab-Bash-script-repo
#Install ssmtp
sudo apt-get install ssmtp

#Access Config file
sudo vim /etc/ssmtp/ssmtp.conf

#Edit Config file
mailhub=smtp.gmail.com:587
useSTARTTLS=YES
AuthUser=username-here
AuthPass=password-here
TLS_CA_File=/etc/pki/tls/certs/ca-bundle.crt

#Bash Script
#!/bin/sh  
SUBJECT="Test Subject"
TO="adekoyapreciouspa@gmail.com"
MESSAGE="Hey There! This is a test mail"

echo $MESSAGE | sudo ssmtp -vvv $TO

#Permission to access file
$ sudo chmod 755 scriptbash.sh 

#Run the app
$ sudo ./scriptbash.sh

# Output
[<-] 220 smtp.gmail.com ESMTP u65sm14952769pfu.104 - gsmtp
[->] EHLO kali
[<-] 250 SMTPUTF8
[->] STARTTLS
[<-] 220 2.0.0 Ready to start TLS
[->] EHLO kali
[<-] 250 SMTPUTF8
[->] AUTH LOGIN
[<-] 334 VXNlcm5edhbAWU6
[->] dmlzaGFsY2hhasd2dWhhbjIyMTJAZ21haWwuY29t
[<-] 334 EUEeGFzc3dvfcaqQ6
[<-] 535 5.7.8  https://support.google.com/mail/?p=BadCredentials u65smyez14952a76922r5pfui.104 - gsmtp
ssmtp: Authorization failed (535 5.7.8  https://support.google.com/mail/?p=BadCredentials u65smyez14952a76922r5pfui.104 - gsmtp)
crazy@kali:~/Documents/Scripts$ 
