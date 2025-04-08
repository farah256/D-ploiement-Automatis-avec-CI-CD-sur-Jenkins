# Déploiement Automatisé d'une Application Web avec Jenkins et AWS

## Partie 1: CI (Continuous Integration)

### 1. Build
#### Création du fichier Dockerfile:
<img width="590" alt="0" src="https://github.com/user-attachments/assets/75c7344c-f434-40bc-a6d8-0c9602917d07" />

#### Construction de l'image Docker:
<img width="971" alt="1" src="https://github.com/user-attachments/assets/af88932d-246b-4f4c-b54d-16a318d19e6b" />
<img width="895" alt="2" src="https://github.com/user-attachments/assets/59bae6bd-de40-4f06-b44b-bc535f1d6467" />

### 2. Test
#### Création du conteneur:
<img width="1067" alt="3" src="https://github.com/user-attachments/assets/f4651afe-a0ee-4304-aeb6-de178c727d01" />
<img width="1080" alt="4" src="https://github.com/user-attachments/assets/72fac4af-579d-458f-aa58-8443cce08e82" />

#### Vérification de l'application:
- Accès via http://localhost:8080  
<img width="446" alt="5" src="https://github.com/user-attachments/assets/3eb1738e-42e9-4e45-855e-19dccc12fee3" />

#### Test avec CURL
<img width="861" alt="6" src="https://github.com/user-attachments/assets/8f736a4e-c718-4902-8103-6a5d47fc0b68" />

### 3. Release
#### Connexion à Docker Hub:
<img width="930" alt="7" src="https://github.com/user-attachments/assets/c2e8ccb9-dee2-40df-b65e-83a4ad10a602" />

#### Push de l'image:
<img width="944" alt="8" src="https://github.com/user-attachments/assets/72be0ba7-7e27-422f-80d6-106e976b4a88" />
<img width="869" alt="9" src="https://github.com/user-attachments/assets/f0d1b7a2-25d1-426e-834d-70f2883efa6a" />

#### Vérification finale:
<img width="1198" alt="10" src="https://github.com/user-attachments/assets/15876f56-5ae3-4c9e-bd1e-94ab39e106fe" />

## Partie 2: CD (Continuous Deployment)
<img width="953" alt="11" src="https://github.com/user-attachments/assets/b7d40366-c2da-4f79-9c99-0508bace20a8" />

## Description du Pipeline CD
Ce pipeline Jenkins déploie automatiquement l'application sur trois environnements :

1. **Review** (port 8080) - Environnement de test initial
2. **Staging** (port 8081) - Pré-production
3. **Production** (port 80) - Simulation de production

