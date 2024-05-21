# Docker-project
## what do if we forget jenkins password
1. we contact jenkins admin for our logins#1
## if system admin forgets jenkins password then ?
Admin, login as Default User of jenkins and changes admins logins
## if default user loses logins then ?
cd /var/lib/jenkins/
vim config.xml
then change userSecurity from true to false and save
systemctl restart jenkins
now jenkins won't ask for login and after login --> manage jenkins-->security-->security realm -->jenkins own user database and save
go to users -->configure change password
go to security again -->authorization: logged in users can do anything and save 
now it's ask for logins and login with conditionals
## if Username forgets
cd /var/lib/jenkins/users/ 
user.xml can be seen in this file
