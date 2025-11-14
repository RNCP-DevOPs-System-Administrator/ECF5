# RNCP DevOps System Administrator
[Evaluation en cours de Formation ECF5](RNCP_DEVOPS-ECF5.pdf)

#  🧪 PREPARER UN ENVIRONNEMENT DE TEST

## 🚀 Node.js + ANSIBLE + TERRAFORM Deployment

### ⚙️ Création branche "TEST" sur  le VCS et une "Organisation Test" sur TERRAFORM Cloud

### 🌍 Dans l’organisation TEST créer un WORKSPACE connecté à la branche "TEST" du repository

### 🛠 Créer une application node.js

- Faire tourner l’application sur la machine pour être sûr qu’elle marche comme souhaité
  ```bash
  - https://nodejs.org/en/docs/guides/getting-started-guide/
  - https://nodejs.org/en/download/
  ```
- Faire en sorte que la réponse à la requête “/” contient la variable d'environnement ENVIRONMENT_NAME.
Voir le paquet npm nommée “dotenv”

### 📚 Provisionner un playbook Ansible dépendant de l’instance qui devra :
- Update et upgrade les paquets à l’initialisation
- Installer nginx et nodejs
- Créer un fichier de configuration nginx mettant en place un reverse proxy redirigeant les requêtes reçus au port 80 vers localhost :3000
- Lancer nginx
- Ajouter une variable d'environnement nommée ENVIRONMENT_NAME qui dans la branche test aura la valeur test et sur master (main) la valeur prod
- Lancer l’application avec nodejs sur le port 300
- Lancez les workflows prod et test, vérifier l'accès aux deux sites web, l’un renvoyant un message contenant le mot test et l’autre prod

## 🎯 Livrables : Deux serveurs chacun dans un environnement différent consultable via internet et facilement différenciable
```bash
- Test: http://<IP_TEST>
- Prod: http://<IP_PROD>
```
