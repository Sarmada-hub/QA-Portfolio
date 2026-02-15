# Cas de test : Réservation de RDV

Projet : SaaS de gestion de RDV médicaux (fictif)  
Module : Réservation de rendez-vous   
Auteur : Sarmada MOHAMED  
Version : 1.1  

---

# CT-RDV-001 : Accès à la page de réservation
**Priorité :** Haute  
**Type :** Test fonctionnel  

**Préconditions :**
- Patient connecté

**Etapes :** 
1. Depuis le table de bord, cliquer sur "Prendre un rendez-vous"

**Résultat attendu :**
- La page de réservation s'affiche
- Les champrs de recherche praticien, créneaux sont visibles

---

## CT-RDV-002 : Affichage des créneaux disponibles après sélection praticien
**Priorité :** Critique  
**Type :** Test fonctionnel  

**Préconditions :**  
- Patient connecté
- Un praticien "Dr. Test" existe ave des créneaux disponibles

**Données de test :** 
- Praticien : Dr. Test

**Etpaes :**  
1. Accéder à la page de réservation
2. Recherche "Dr. Test"
3. Sélectionner le praticien

**Résultat attendu :**  
- Les créneaux disponibles s'affichent
- Les créneaux indisponibles sont non sélectionnables ou non affichés

---

## CT-RDV-003 : Réservation d'un rendez-vous sur un créneau disponible
**Priorité :** Critique  
**Type :** Test fonctionnel  

**Préconditions :**  
- Patient connecté
- Créneau disponible, exemple : 01/10/2026 à 10h30

**Données de test :**
- Praticien : Dr. Test
- Motif : Consultation de médecine générale
- Créneau : 01/10/2026 à 10h30
- Email du patient : test@gmail.com

**Etapes :**
1. Accéder à "Prendre un rendez-vous"  
2. Sélectionner le praticien "Dr. Test"  
3. Sélectionner le motif "Consiltation de médecine générale"  
4. Choisir le créneau 01/10/2026 à 10h30  
5. Vérifier ou compléter les informations patients requises  
6. Cliquer sur "Confirmer"

**Résultat attendu :**  
- Message "Rendez-vous confirmé"
- RDV visible dans l'onglet "Mes rendez-vous"
- Le créneau n'est plus disponible pour une nouvelle réservation
- Une confirmation est envoyée par email, SMS

---

## CT-RDV-004 : Réservation refusée si créneau déjà reservé
**Priorité :** Critique  
**Type :** Test fonctionnel   

**Préconditions :**  
- Patient connecté
- Le créneau choisi est déjà réservé par un autre patient

**Etapes :**  
1. Accéder à la réservation
2. Sélectionner le praticien
3. Tenter de sélectionner un créneau déjà réserver

**Résultat attendu :** 
- Réservation impossible
- Message explicite "créneau indisponible"  
- Aucun RDV créé

---

## CT-RDV-005 : Annulation d'un rendez-vous par le patient
**Priorité :** Haute  
**Type :** Test fonctionnel  

**Préconditions :**  
- Patient connecté
- Un RDV confirmé existe

**Etapes :**  
1. Aller dans "Mes rendez-vous"
2. Sélectionner le rendez-vous
3. Cliquer sur "Annuler"
4. Confirmer l'annulation

**Résultat attendu :**  
- RDV passe au statut "Annulé"
- Le créneau est libéré
- Notification envoyée au praticien  
- Mail et sms envoyés au patient

---

## CT-RDV-006 : Tentative de réservation sans authentification
**Priorité :** Critique  
**Type :** Test de sécurité

**Préconditions :**  
- Aucun utilisateur connecté

**Etapes :**  
1. Tenter d'accéder à la réservation

**Résultat attendu :**  
- Redirection vers "Connexion"
- Aucune action de réservation possible  
