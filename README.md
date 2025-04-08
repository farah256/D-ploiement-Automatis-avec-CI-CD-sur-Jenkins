# Déploiement Automatisé d'une Application Web avec Jenkins et AWS
## Partie 1: CI (Continuous Integration)
### 1.Build :
#### Creation du fichier Dockerfile:
<img width="971" alt="0" src="https://github.com/user-attachments/assets/97f0e6f2-794d-45dd-918f-bfe676886cb1" />
#### Construire une image:
<img width="971" alt="1" src="https://github.com/user-attachments/assets/97f0e6f2-794d-45dd-918f-bfe676886cb1" />
<img width="895" alt="2" src="https://github.com/user-attachments/assets/59bae6bd-de40-4f06-b44b-bc535f1d6467" />
### 2.Test :
#### Construire un conteneur:
<img width="1067" alt="3" src="https://github.com/user-attachments/assets/f4651afe-a0ee-4304-aeb6-de178c727d01" />
<img width="1080" alt="4" src="https://github.com/user-attachments/assets/72fac4af-579d-458f-aa58-8443cce08e82" />
#### Vérification du lien http://localhost:8080:
<img width="446" alt="5" src="https://github.com/user-attachments/assets/3eb1738e-42e9-4e45-855e-19dccc12fee3" />
#### Tester la disponibilité avec CURL :
<img width="861" alt="6" src="https://github.com/user-attachments/assets/8f736a4e-c718-4902-8103-6a5d47fc0b68" />
### 3. Release
#### Connecter au Docker hub:
<img width="930" alt="7" src="https://github.com/user-attachments/assets/c2e8ccb9-dee2-40df-b65e-83a4ad10a602" />
#### Pousser l'image:
<img width="944" alt="9" src="https://github.com/user-attachments/assets/72be0ba7-7e27-422f-80d6-106e976b4a88" />
<img width="869" alt="8" src="https://github.com/user-attachments/assets/f0d1b7a2-25d1-426e-834d-70f2883efa6a" />
#### Vérification
<img width="1198" alt="10" src="https://github.com/user-attachments/assets/15876f56-5ae3-4c9e-bd1e-94ab39e106fe" />

## Partie 2 : CD (Continuous Deployment)
<img width="953" alt="11" src="https://github.com/user-attachments/assets/b7d40366-c2da-4f79-9c99-0508bace20a8" />
Ce pipeline Jenkins déploie automatiquement une application Docker sur trois environnements : Review (port 8080), Staging (port 8081) et Production (port 80). Chaque étape lance un conteneur temporaire (--rm) à partir de la même image Docker (farahsalmi02996/greeting_app:latest), permettant de tester et valider progressivement l'application avant sa mise en production.
