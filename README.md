

# Modernisation et Sécurisation du Projet Node Authentication

## Contexte
Ce projet consiste en la mise à jour et la sécurisation de l'application **node-authentication**, en suivant deux étapes principales :

1. **Analyse des bibliothèques en obsolescence (SCA - Software Composition Analysis)** sur la variante `Lvl 1. Plain Text Passwords`.
2. **Rénovation et modernisation de la composition logicielle** sur la variante `Lvl 6. OAuth`, en appliquant des corrections de vulnérabilités et en mettant à jour les dépendances obsolètes.

---

## **1. Analyse des Bibliothèques en Obsolescence (SCA)**

### **Objectif**
Identifier au moins deux bibliothèques en obsolescence dans `Lvl 1. Plain Text Passwords` et proposer la version la plus récente à privilégier.

### **Démarche**
1. Exécution de la commande suivante pour analyser les bibliothèques obsolètes :
   ```bash
   npm outdated
   ```
2. Identification des bibliothèques nécessitant une mise à jour.

### **Résultats**
| Bibliothèque      | Version actuelle | Version recommandée |
|------------------|-----------------|---------------------|
| `express`       | 4.17.1          | 4.21.2              |
| `mongoose`      | 5.9.10          | 8.12.1              |

**Pourquoi mettre à jour ?**
- `express` : Corrections de bugs, optimisations et corrections de vulnérabilités.
- `mongoose` : Amélioration des performances et des fonctionnalités, correction de failles de sécurité.

---

## **2. Modernisation de la Composition Logicielle (Lvl 6. OAuth)**

### **Objectif**
Mettre à jour les dépendances et sécuriser l'application.

### **Étapes réalisées**

#### **Étape 1 : Élimination des risques de vulnérabilités**
1. Exécution de :
   ```bash
   npm audit fix --force
   ```
2. Correction des vulnérabilités critiques détectées.
3. **Commit des corrections** :
   ```bash
   git add .
   git commit -m "Correction des vulnérabilités détectées avec npm audit"
   ```

#### **Étape 2 : Mise à jour des bibliothèques obsolètes**
1. Vérification des dépendances obsolètes :
   ```bash
   npm outdated
   ```
2. Mise à jour des packages :
   ```bash
   npm update
   ```
3. **Commit des mises à jour** :
   ```bash
   git add .
   git commit -m "Mise à jour des dépendances obsolètes pour assurer la compatibilité avec les versions récentes"
   ```

#### **Étape 3 : Push des modifications sur GitHub**
1. Vérification de la configuration du remote :
   ```bash
   git remote -v
   ```
2. Ajout de l'origine vers la fork :
   ```bash
   git remote set-url origin https://github.com/LoaneCTLL/node-authentication.git
   ```
3. Poussée des modifications sur GitHub :
   ```bash
   git push -u origin main
   ```

---

## **Résultat Final**
Le projet a été sécurisé et modernisé en corrigeant les vulnérabilités et en mettant à jour les bibliothèques obsolètes. 

Lien du dépôt mis à jour : [node-authentication-modernized](https://github.com/LoaneCTLL/node-authentication)

---


## Node Authentication

This is a step-by-step tutorial repository which guides about the various type of authentication techniques that can be used in Node.js right from Plain Text Passwords to encryption, hashing, salting and oAuth.
<br><br>

If you would like to download the code and try it for yourself:

### Instructions
1. Clone the repo: <pre>git clone https://github.com/ishandeveloper/node-authentication.git</pre>
1. Move to desired folder using: <code>cd\\[Desired Folder]</code>
1. Install packages: <code>npm install</code>
    ##### (<b>Important</b>)  Repositories beyond Lvl 2. require SECRET encryption key. So make sure to create a <code>.env</code> file with the following format.

        SECRET="YOUR ENCRYPTION KEY STRING"


1. Launch using : <code>npm start</code>
1. Visit in your browser at: http://localhost:8080


##### Written with ♥ by <a href="https://github.com/ishandeveloper">ishandeveloper</a>


[![forthebadge](https://forthebadge.com/images/badges/built-with-love.svg)](https://github.com/ishandeveloper)


## Node Authentication

This is a step-by-step tutorial repository which guides about the various type of authentication techniques that can be used in Node.js right from Plain Text Passwords to encryption, hashing, salting and oAuth.
<br><br>

If you would like to download the code and try it for yourself:

### Instructions
1. Clone the repo: <pre>git clone https://github.com/ishandeveloper/node-authentication.git</pre>
1. Move to desired folder using: <code>cd\\[Desired Folder]</code>
1. Install packages: <code>npm install</code>
    ##### (<b>Important</b>)  Repositories beyond Lvl 2. require SECRET encryption key. So make sure to create a <code>.env</code> file with the following format.

        SECRET="YOUR ENCRYPTION KEY STRING"


1. Launch using : <code>npm start</code>
1. Visit in your browser at: http://localhost:8080


##### Written with ♥ by <a href="https://github.com/ishandeveloper">ishandeveloper</a>


[![forthebadge](https://forthebadge.com/images/badges/built-with-love.svg)](https://github.com/ishandeveloper)
