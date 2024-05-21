# Docker-project

Steps: 
1. CODE--> Git#1
2. SCAN--> SONARQUBE(CQA)#2
3. npm install dependencies#3
4. OWASP--> to check if dependencies were installed#4
5. Image Build--> Docker#5
6. Image Scan --> Trivy#6
7. DockerHub#7
8. Deploy container#8
--------------------------------------------------------------------------------------------------------------------------------------------------
## what if we forget jenkins password
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
