# vprofile_freestyle_jenkins
# Goal to create a JOB in jenkins for vprofile project:
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

## Go to create job and create a freestyle config

<img width="1552" alt="image" src="https://github.com/Kamalesh-Seervi/vprofile_freestyle_jenkins/assets/107933310/802fb174-7da5-4879-bded-7bba0b5b7c6c">

- In code source management add the git url of the project repo:

```
https://github.com/devopshydclub/vprofile-project.git
```

- In build steps add maven targets and set the maven version

<img width="1552" alt="image" src="https://github.com/Kamalesh-Seervi/vprofile_freestyle_jenkins/assets/107933310/4081bd1d-9b49-4786-8117-3cb7a58705ad">

- Save and click build now :

<img width="1552" alt="image" src="https://github.com/Kamalesh-Seervi/vprofile_freestyle_jenkins/assets/107933310/f543d2dd-f63c-4c9f-8afb-bb621bc5244c">

- Go to workspace in target folder download vprofile.war 

- If you want to secure the artifacts go to configure under that use Post Build action as Archive artifacts.
- File to Archive 
```
***/*.war
```
- Build Again:

<img width="1552" alt="image" src="https://github.com/Kamalesh-Seervi/vprofile_freestyle_jenkins/assets/107933310/b3be664a-1e8a-4f05-94ec-36e79d81e836">

- Now the `.war` is saved in archive so even if we delete the workspace the .war is already archived .


