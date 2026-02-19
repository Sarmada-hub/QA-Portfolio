# Issue Report : Swag Labs

Projet : Swag Labs  
Application : https://www.saucedemo.com  
Testeur : Sarmada MOHAMED
Date : 14/02/2026

---

## Issue ID
IMP-001

## Type  
Improvment  

## Titre
Absence de masquage explicite du mot de passe lors d'une tentative de connexion invalide

---

## Environnement  
- Application : Swag Labs
- URL : https://www.saucedemo.com
- Navigateur : Google Chrome
- Système d'exploitation : macOS

---  

## Description
Lors de la saisie d'un mot de passe incorrect, le système affiche un message d'erreur générique : "Epic sadface: Username and password do not match any user in this service".  
Ce message n'indique pas clairement quel champ est incorrect.  
Un message plus explicite améliorerait l'expérience utilisateur en facilitant l'identification et la correction de l'erreur.

---

## Préconditions  
- L'utilisateur possède un compte valide
- L'utilisateur n'est pas connecté
- La apge de connexion est accessible

---

## Données de test  
- Username : standard_user
- Password : wrong

---

## Étapes pour reproduire

1. Accéder à l'URL : https://www.saucedemo.com
2. Saisir l'username de test
3. Saisir le password de test 
3. Cliquer sur "Login"

---

## Résultat attendu

Le système doit afficher un message d'erreur clair et précis indiquant que le mot de passe est incorrect.

---

## Résultat observé

Le système affiche le message :
"Epic sadface: Username and password do not match any user in this service"

Le message ne précise pas si le problème vient de l'username ou du password

---

## Sévérité
Faible

--- 

## Priorité
Basse

---

## Statut

Ouvert

---

## Recommandation

Améliorer le message d’erreur afin de fournir une indication plus claire à l’utilisateur, tout en respectant les bonnes pratiques de sécurité.
