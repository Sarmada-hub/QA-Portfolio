# Cas de test : Réserver un RDV

Projet : Application SaaS de gestion de rendez-vous médicaux  
Module : Réservation de rendez-vous  
Auteur : Sarmada MOHAMED  

---

## Objectif

Vérifier que le patient peut réserver, consulter et annuler un rendez-vous conformément aux règles métier.

---

## Cas de test

| ID | Titre | Priorité | Préconditions | Étapes | Résultat attendu |
|----|-------|----------|---------------|--------|------------------|
| TC-APT-01 | Accès à la page de réservation | Haute | Patient connecté | Accéder à la section réservation | Page affichée correctement |
| TC-APT-02 | Affichage des créneaux disponibles | Critique | Patient connecté | Sélectionner un praticien | Créneaux disponibles affichés |
| TC-APT-03 | Réservation d’un créneau valide | Critique | Patient connecté | Sélectionner un créneau et confirmer | Rendez-vous enregistré |
| TC-APT-04 | Tentative de réservation d’un créneau indisponible | Critique | Créneau déjà réservé | Sélectionner ce créneau | Message d’erreur affiché |
| TC-APT-05 | Annulation d’un rendez-vous | Haute | Rendez-vous existant | Cliquer sur annuler | Rendez-vous annulé |
| TC-APT-06 | Réservation sans connexion | Critique | Patient non connecté | Accéder à la réservation | Redirection vers connexion |

---

## Risques couverts

- Double réservation
- Accès non autorisé
- Perte de données
- Mauvaise gestion des créneaux
