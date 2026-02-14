# Cas de test – Accès & Authentification
Projet : SaaS RDV médicaux   
Module : Authentification / Gestion de session / Contrôle d’accès  
Auteur : Sarmada MOHAMED  

## Hypothèses & périmètre
- Rôles : Patient, Praticien, Admin 
- Navigateurs cibles : Chrome, Firefox 

## Table des cas de test manuel

| ID | Titre | Priorité | Préconditions | Étapes | Résultat attendu |
|---|---|---|---|---|---|
| TC-ACC-01 | Accès à la page d’accueil sans connexion | Haute | Aucun utilisateur connecté | 1. Ouvrir l’URL de la plateforme | La page publique s’affiche. Les actions protégées demandent une connexion. Boutons Connexion/Inscription visibles. |
| TC-ACC-02 | Connexion avec identifiants valides | Critique | Compte patient existant | 1. Aller à Connexion 2. Saisir email valide 3. Saisir MDP valide 4. Cliquer “Se connecter” | Redirection vers le tableau de bord. Nom/compte visible. Session active. |
| TC-ACC-03 | Connexion refusée avec mot de passe incorrect | Haute | Compte patient existant | 1. Aller à Connexion 2. Saisir email valide 3. Saisir MDP incorrect 4. Cliquer “Se connecter” | Connexion refusée. Message d’erreur explicite. Aucun accès aux pages protégées. |
| TC-ACC-04 | Accès direct à une page protégée sans être connecté | Critique | Aucun utilisateur connecté | 1. Saisir directement l’URL `/dashboard` | Redirection vers Connexion. Aucun contenu protégé affiché. |
| TC-ACC-05 | Déconnexion utilisateur | Haute | Utilisateur connecté | 1. Cliquer “Déconnexion” | Redirection vers Connexion. Session terminée. |
| TC-ACC-06 | Accès à une page protégée via bouton “Retour” après déconnexion | Critique | Utilisateur connecté puis déconnecté | 1. Se déconnecter 2. Cliquer “Retour” navigateur | Accès refusé. Redirection Connexion ou page publique. Pas de données affichées. |

---

## Notes 
- Tests couvrant : authentification, contrôle d’accès, gestion de session
- Prochaines extensions : session expirée, verrouillage après X tentatives, rôles Praticien/Admin, accessibilité (messages d’erreur), RGPD (données personnelles)
