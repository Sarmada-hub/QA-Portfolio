# Cas de test : Accès & Authentification
Projet: SaaS RDV médicaux (fictif)  
Module: Authentification / Gestion de session / Contrôle d’accès    
Auteur: Sarmada MOHAMED   
Version: 1.1  

---

## CT-ACC-001 : Accès à la page d'accueil sans authentification  
**Priorité :** Haute  
**Type :** Fonctionnel  

**Préconditions :**
- Aucun utilisateur connecté (session vide)  

**Données de test :**  
- URL : Page d'accueil publique  

**Etapes :**
1. Ouvrir l'URL de la plateforme
2. Observer la page affichée

**Résultat attendu:**
- La page d'accueil publique s'affiche  
- Les actions protégées (ex: réserver/RDV) ne sont pas accessibles  
- Un bouton "Connexion/Inscription" est visible  

---

## CT-ACC-002 : Connexion avec identifiants valides  
**Priorité :** Critique  
**Type :** Fonctionnel positif  

**Préconditions :**   
- Un compte patient existe et est actif  

**Données de test :**  
- Email : test@gmail.com  
- Mot de passe : Passtest3!  

**Etapes :**
1. Accéder à la page "Connexion"
2. Saisir l'email de test
3. Saisir le mot de passe de test
4. Cliquer sur "Se connecter"

**Résultat attendu :**
- L'utilisateur est authentifié  
- Redirection vers le tableau de bord  
- La session est active  

---

## CT-ACC-003 : Connexion refusée dû à un mot de passe incorrect
**Priorité :** Haute  
**Type :** Fonctionnel négatif 

**Préconditions :**
- Un compte patient existe

**Données de test :**
- Email : test@gmail.com
- Mot de passe : erreur

**Etapes :**
1. Accéder à la page "Connexion"
2. Saisir l'email de test
3. Saisir le mot de passe de test
4. Cliquer sur "Se connecter"

**Résultat attendu :**
- L'utilisateur ne parvient pas à s'authentifier
- Message d'erreur explicite affiché
- Aucun accès au tableau de bord
- La session n'est pas active

---

## CT-ACC-004 : Inscription avec mot de passe valide
**Priorité :** Haute  
**Type :** Fonctionnel positif

**Préconditions :**
- Aucun utilisateur connecté
- L'adresse mail utilisée n'est pas déjà associée à un compte existant
- La page "Inscription" est accessible

**Données de test :**
- Email : test.qa@gmail.com
- Mot de passe : QaTest1!

**Etapes:**
1. Accéder à la page "Inscription"
2. Saisir l'email de test
3. Saisir le mot de passe de test
4. Cliquer sur "Créer un compte"

**Résultat attendu :**
- Un message informe l'utilisateur qu'un email de confirmation a été envoyé
- Après conformation via le lien reçu par email :  
l'utilisateur est redirigé vers le tableau de bord  
le compte est activé  
la session est active   

---

## CT-ACC-005 : Inscription avec mot de passe invalide
**Priorité :** Haute  
**Type :** Fonctionnel négatif

**Préconditions :**
- Aucun utilisateur connecté
- L'adresse mail utilisée n'est pas déjà associée à un compte existant
- La page "Inscription" est accessible

**Données de test :**
- Email : qa.test@gmail.com
- Mot de passe : nonvalide

**Etapes :**
1. Accéder à la page "Inscription"
2. Saisir l'email de test
3. Saisis le mot de passe de test

**Résultat attendu:**  
- Inscription refusée  
- Message d'erreur explicite affiché indiquant que le mot de passe ne respecte pas les critères requis  
- Aucun compte n'est créé  
- L'utilisateur reste sur la page d'inscription

---  

## CT-ACC-006 : Accès direct à une page protégée sans être connecté
**Priorité :** Critique  
**Type :** Contrôle d'acès, sécurité

**Préconditions :**
- Aucun utilisateur conencté

**Données de test :**
- URL protégée

**Etapes :**
1. Saisir directement l'URL protégée dans le navigateur
2. Valider

**Résultat attendu :**  
- Redirection vers la page "Connexion"  
- Aucun contenu protégé visible  

---

## CT-ACC-007 : Accès via retour navigateur après déconnexion 
**Priorité :** Critique  
**Type :** Gestion de session

**Préconditions :**
- Utilisateur connecté puis déconnecté

**Etapes :**
1. Se déconnecter
2. Cliquer sur le bouton "retour" du navigateur

**Résultat attendu :**
- Accès refusé aux pages protégées  
- Redirection vers "Connexion" ou page publique  
- Aucune donnée sensible affichée  
