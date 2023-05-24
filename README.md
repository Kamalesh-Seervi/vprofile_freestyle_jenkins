# vprofile_freestyle_jenkins
### This repo uses EC2 instance and installed jenkins 

```
curl -fsSL https://pkg.jenkins.io/debian/jenkins.io-2023.key | sudo tee \
  /usr/share/keyrings/jenkins-keyring.asc > /dev/null
echo deb [signed-by=/usr/share/keyrings/jenkins-keyring.asc] \
  https://pkg.jenkins.io/debian binary/ | sudo tee \
  /etc/apt/sources.list.d/jenkins.list > /dev/null
sudo apt-get update
sudo apt-get install jenkins
```

# Tools Required 
- EC2 instance ( Use only Ubuntu 20:latest)
- jenkins 
- maven 
- openjdk 8
```
sudo apt install openjdk-8-jdk -y
```
- git
