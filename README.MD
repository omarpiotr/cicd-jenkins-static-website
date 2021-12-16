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