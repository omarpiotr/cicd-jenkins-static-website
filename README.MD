[![Build Status](http://54.144.136.33:8080/buildStatus/icon?job=cicd-jenkins-static-website)](http://54.144.136.33:8080/job/cicd-jenkins-static-website/)
# COMPTE RENDU
* Mise en place d'un Pipline CI/CD à l'aide de Jenkins.
* Déploiement sur des machines ubuntu (avec docker) sur AWS
* WebHook avec Git

# 2 machines Ubuntu identiques EC2 sur AWS
* Production
* Staging
```bash
#!/bin/bash
curl -fsSL https://get.docker.com -o get-docker.sh
sh get-docker.sh
usermod -aG docker ubuntu
systemctl start docker
sudo systemctl enable docker 
```
* omar-ec2-dk-staging : 18.233.10.235
* omar-ec2-dk-prod : 3.93.241.97


