# DevOps-Project
guide to set up a ci/cd workflow 
https://www.ktexperts.com/how-to-install-jenkins-in-amazon-linux-machine/


- Launch Jenkins Machine. 
- Connect to Jenkins Linux EC2 Terminal through MobaXterm.
- Switch to root user.  
```
sudo su
```
- Update Server Packages.
```
yum update -y
```

- Install the Java. 
```
amazon-linux-extras install epel -y 
amazon-linux-extras install java-openjdk11
java -version
```

- Download and Install Jenkins. 
```
yum -y install wget
wget -O /etc/yum.repos.d/jenkins.repo https://pkg.jenkins.io/redhat-stable/jenkins.repo
rpm --import https://pkg.jenkins.io/redhat-stable/jenkins.io.key
yum -y install jenkins
```
- Start the Jenkins.
```
systemctl start jenkins
chkconfig jenkins on
```
- Access the Jenkins.

By default jenkins runs at port 8080, You can access jenkins at
```
http://YOUR-SERVER-PUBLIC-IP:8080
```