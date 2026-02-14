# Bug Report – Swag Labs

Testeur : Sarmada MOHAMED  
Application : https://www.saucedemo.com  
Date : 14/02/2026
Environnement : Chrome / Mac 

---

## Bug ID
BUG-001

## Titre
Absence de masquage explicite du mot de passe lors d'une tentative de connexion invalide

## Description
Lors de la saisie d'un mot de passe incorrect, le message d'erreur affiché n'indique pas clairement quel champ est incorrect, ce qui peut générer une confusion pour l'utilisateur.

## Étapes pour reproduire

1. Accéder à https://www.saucedemo.com
2. Entrer :
   Username : standard_user
   Password : secret
3. Cliquer sur Login

## Résultat attendu

Le système doit afficher un message d'erreur clair et précis indiquant que le mot de passe est incorrect.

## Résultat observé

Le système affiche le message :
"Epic sadface: Username and password do not match any user in this service"

Le message ne précise pas si le problème vient de l'username ou du password.

## Sévérité
Faible

## Priorité
Basse

## Statut
Ouvert
