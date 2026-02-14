# Test Execution – Swag Labs

Application testée : https://www.saucedemo.com  
Type : Application web e-commerce  
Testeur : Sarmada MOHAMED  

---

## Objectif

Exécuter des tests manuels sur une application réelle afin de valider les fonctionnalités critiques.

---

## Environnement

- Navigateur : Chrome
- OS : Mac 
- Date : 14/02/2026

---

## Tests exécutés

### TEST-EXE-01 : Connexion avec identifiants valides

Étapes :
1. Accéder à https://www.saucedemo.com
2. Saisir :
   Username : standard_user
   Password : secret_sauce
3. Cliquer sur Login

Résultat attendu :
Connexion réussie, accès à la page inventaire

Résultat observé :
Connexion réussie, accès à la page produits 

Statut :
PASS

---

### TEST-EXE-02 : Connexion avec identifiants invalides

Étapes :
1. Saisir un mauvais mot de passe
   Username : standard_user
   Password : secret!
3. Cliquer sur Login

Résultat attendu :
Message d'erreur affiché

Résultat observé :
Message d'erreur affiché "Epic sadface: Username and password do not match any user in this service"

Statut :
FAIL
