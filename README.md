# TP2 – GitHub Actions  
**KHARROUB YASSER – EMSI Tanger**

Ce dépôt contient la réalisation du **TP2 DevOps : GitHub Actions**.  
L’objectif du TP est de configurer un workflow CI (Continuous Integration) permettant :

- La compilation automatique d’un projet Android  
- L’exécution des tests unitaires  
- La validation automatique après chaque **push** et chaque **pull request**  
- La détection automatique d’erreurs dans le build ou les tests

---

##  1. Création du Workflow GitHub Actions

Nous avons d’abord créé un fichier de workflow dans :

.github/workflows/android-ci.yml

<img width="975" height="548" alt="image" src="https://github.com/user-attachments/assets/982cad4f-0539-4a69-b697-ae1f24d04737" />
<img width="975" height="548" alt="image" src="https://github.com/user-attachments/assets/6c6df337-a8fd-4d08-8d41-00329c84620b" />

##  2. Création du projet Android & premier push

Après avoir généré le projet Android, nous l'avons poussé sur GitHub.
Dès le premier push, le workflow s'est exécuté automatiquement.

✔️ Création du projet Android

<img width="975" height="548" alt="image" src="https://github.com/user-attachments/assets/5a0bd0c2-3ae4-4e68-b2b3-5bbcbeffb236" />


✔️ Dépôt GitHub après push

<img width="975" height="548" alt="image" src="https://github.com/user-attachments/assets/6f3b94f9-3d48-4ede-8829-5dbca4d4163b" />


✔️ Détection automatique par GitHub Actions

Le workflow commence automatiquement :

<img width="975" height="548" alt="image" src="https://github.com/user-attachments/assets/eb99baf8-489e-4f36-ba7c-6650dfba0b35" />

## 3. Test Unitaire & Déclenchement du workflow
   
on va ajouter les test unitere a workflow : 
<img width="859" height="741" alt="image" src="https://github.com/user-attachments/assets/9a035b65-426b-48f7-bdc8-d831dff3566d" />

Nous avons modifié le fichier *ExampleUnitTest* pour provoquer une erreur volontaire :
<img width="975" height="202" alt="image" src="https://github.com/user-attachments/assets/b003feb8-14e3-44f7-9b1d-b6903335b5a9" />


Après push, GitHub Actions détecte l’erreur :
<img width="975" height="112" alt="image" src="https://github.com/user-attachments/assets/139b05dd-9f31-4b7e-b8be-4bdee1a60122" />
.
<img width="975" height="523" alt="image" src="https://github.com/user-attachments/assets/c1ea13a6-f5b7-4f64-9dee-585830133ded" />
.
<img width="975" height="498" alt="image" src="https://github.com/user-attachments/assets/8c6f448b-d6ca-42eb-b174-9182a8d24ae5" />

## 4. Correction des tests
Après un nouveau push :
Le workflow se relance automatiquement
Les tests passent avec succès
GitHub affiche All checks have passed
<img width="975" height="548" alt="image" src="https://github.com/user-attachments/assets/b699a88e-f831-4352-849b-288caa5d4f3f" />
<img width="975" height="94" alt="image" src="https://github.com/user-attachments/assets/9920293e-c7d7-40b8-b504-af667cbb7c9d" />
<img width="975" height="497" alt="image" src="https://github.com/user-attachments/assets/95e93bfa-ff0a-4d73-a6da-c8a432011e76" />

## 5. Résultat Final


Grâce au workflow GitHub Actions :

✔ Compilation Android automatisée

✔ Exécution des tests unitaires

✔ Détection des erreurs

✔ Validation automatique dans les Pull Requests

Ce TP montre comment mettre en place une intégration continue simple mais complète pour un projet Android via GitHub Actions.

 ## Auteur

KHARROUB YASSER
Étudiant en Ingénierie Informatique & Réseaux – EMSI Tanger
