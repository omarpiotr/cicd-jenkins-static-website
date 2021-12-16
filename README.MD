[![Build Status](http://54.144.136.33:8080/buildStatus/icon?job=cicd-jenkins-static-website)](http://54.144.136.33:8080/job/cicd-jenkins-static-website/)
# COMPTE RENDU
Mise en place d'un Pipline CI/CD à l'aide de Jenkins.<br>
Déploiement sur des machines ubuntu (avec docker) sur AWS

# Création de 2 machines EC2 destinée
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


# Configuration de Jenkins
* Création d'un Projet Pipline lié à notre GitHub

ssh -o StrictHostKeyChecking=no -i ${keyfile} ${NUSER}@${EC2_STAGING_HOST} docker stop $CONTAINER_NAME && docker rm $CONTAINER_NAME && docker run --name $CONTAINER_NAME -d -e PORT=5000 -p 5000:5000 $USERNAME/$IMAGE_NAME:$BUILD_TAG

ssh -o StrictHostKeyChecking=no -i ${keyfile} ${NUSER}@${EC2_STAGING_HOST} docker rm $CONTAINER_NAME
ssh -o StrictHostKeyChecking=no -i ${keyfile} ${NUSER}@${EC2_STAGING_HOST} docker run --name $CONTAINER_NAME -d -p 5000:5000 $USERNAME/$IMAGE_NAME:$BUILD_TAG





ssh -o StrictHostKeyChecking=no -i ${keyfile} ${NUSER}@${EC2_STAGING_HOST} docker stop $CONTAINER_NAME && docker rm $CONTAINER_NAME && docker run --name $CONTAINER_NAME -d -e PORT=5000 -p 5000:5000 $USERNAME/$IMAGE_NAME:$BUILD_TAG

ssh -o StrictHostKeyChecking=no -i ${keyfile} ${NUSER}@${EC2_STAGING_HOST} docker rm $CONTAINER_NAME

ssh -o StrictHostKeyChecking=no -i ${keyfile} ${NUSER}@${EC2_STAGING_HOST} docker run --name $CONTAINER_NAME -d  -p 5000:5000 $USERNAME/$IMAGE_NAME:$BUILD_TAG
                        '