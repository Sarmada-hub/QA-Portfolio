# Exécution de tests : Swag Labs

**Application testée :** https://www.saucedemo.com  
**Type :** Application web e-commerce  
**Testeur :** Sarmada MOHAMED  
**Date d'exécution :** 14/02/2026

---

## 1. Objectif

Vérifier le bon fonctionnement du module d'authentification en exécutant des tests manuels sur une application réelle  
- Connexion avec identifiants valides
- Gestion des erreurs lors la connexion avec identifiants invalides  

---

## 2. Environnement de test

- **Navigateur :** Google Chrome  
- **Système d'exploitation :** macOS
- **Type de test:** Test manuel  

---

## 3. Tests exécutés

### ET-001 : Connexion avec identifiants valides

**Priorité :** Critique  
**Type :** Test fonctionnel positif  

**Préconditions :**  
- L'utilisateur possède un compte valide
- L'utilisateur n'est pas connecté
- La page de connexion est accessible

**Données de test :**  
- Username : standard_user
- Passwod : secret_sauce

**Étapes :**
1. Accéder à l'URL : https://www.saucedemo.com  
2. Saisir l'username : standard_user  
3. Saisir le password : secret_sauce  
4. Cliquer sur "Login"  

**Résultat attendu :**
- Le système authentifie l'utilisateur
- L'utilisateur est redirigé vers la page produit
- La liste de produits est affichée  

**Résultat observé :**  
- Le système authentifie correctement l'utilisateur
- Redirection vers la page inventaire
- La liste de produits est affichée sans erreur
  
**Statut :** PASS

---

### ET-002 : Connexion avec identifiants invalides

**Priorité :** Critique  
**Type :** Test fonctionnel négatif  

**Préconditions :**  
- L'utilisateur possède un compte valide
- L'utilisateur n'est pas connecté
- La page de connexion est accessible

**Données de test :**  
- Username : standard_user
- Password : wrong

**Étapes :**  
1. Accéder à l'URL : https://www.saucedemo.com
2. Saisir l'username de test
3. Saisir le password de test
4. Cliquer sur "Login"

**Résultat attendu :**
- Le système refuse la connexion
- Un message d'erreur s'affiche
- L'utilisateur reste sur la page de connexion
- Aucune session n'est créée  

**Résultat observé :**
- Le système refuse la connexion  
- Le message d'erreur suivant s'affiche : "Epic sadface: Username and password do not match any user in this service"  
- L'utilisateur reste sur la page de connexion
- Aucune session n'est créée  

**Statut :** PASS

---

## 4. Conclusion  

Les tests exécutés confirment que le module d'authentificaiton fonctionne conformément aux exigences fonctionnelles attendues :  
- La connexion avec identifiants valides fonctionne correctement
- Le système empêche l'accès avec des identifiants invalides
- Les messages d'erreur sont correctement affichés
- Le contrôle d'accès est correctement appliqué

Aucune anomalie fonctionnelle n'a été identifiée 
