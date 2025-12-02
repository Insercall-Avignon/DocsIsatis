# Liste des formations

## 🎯 Objectif

La page **Liste des formations** permet à chaque utilisateur de **visualiser l’ensemble des sessions de formation** accessibles selon ses droits.  
Elle sert à la fois de point d’entrée vers les détails d’une formation et de base pour effectuer une inscription ou un suivi.

---

## 🧭 Accès

- **Stagiaires** : voient uniquement les sessions ouvertes à l’inscription.
- **Formateurs** : voient les sessions qu’ils animent.
- **Entreprises** : voient les formations où leurs salariés sont inscrits ou peuvent être positionnés.
- **Administrateurs** : voient toutes les sessions existantes, quel que soit leur statut.
  > Les sessions (INTRA et INTER) qui débutent dans moins de 14 jours ne sont pas affichées aux stagiaires et aux entreprises, sauf pour les administrateurs et formateurs concernés.

---

## 🗂️ Présentation de la liste

Les formations sont affichées sous forme de **cartes interactives** ou de **tableaux dynamiques** selon le rôle et la configuration d’affichage.

Chaque **carte de formation** contient :

- Le **titre** de la formation
- Les **dates de début et de fin**
- La **durée totale** (ex. 2 semaines)
- Le **type de session** : **INTRA** (réservée à une entreprise) ou **INTER** (ouverte à plusieurs participants)
- Le **formateur principal**
- Le **statut** de la session (ouverte, complète, terminée, annulée)
- Des **raccourcis** vers :
  - Le détail de la session
  - Le formulaire d’inscription
  - Les documents associés

> 💡 Les sessions terminées apparaissent dans une section “historique” pour consultation des documents uniquement.

---

## 🔍 Recherche et filtres

Le système de recherche permet de filtrer les formations par :

- Nom de la formation
- Formateur
- Date
- Statut (ouverte, en cours, terminée)
- Type de session (**INTRA / INTER**)

> Les filtres sont **cumulables** et **compatibles avec la pagination**.

---

## 📅 Statuts de session

| Statut          | Description                                                     |
| --------------- | --------------------------------------------------------------- |
| 🟢 **Ouverte**  | La formation est disponible à l’inscription                     |
| 🟠 **En cours** | La session est active (formation en déroulement)                |
| 🔵 **Terminée** | La session est clôturée mais ses documents restent consultables |
| 🔴 **Annulée**  | La session a été annulée (visible uniquement par les admins)    |

---

## 🧾 Détails d’une session

En cliquant sur une formation, l’utilisateur accède à la **fiche détaillée** contenant :

- Description de la formation
- Objectifs pédagogiques
- Programme et durée (**ex. 2 semaines**)
- Type de session : **INTRA / INTER**
- Liste des participants (selon les rôles)
- Documents associés (fiche d’inscription, feuilles d’émargement, questionnaires…)

> 📎 Les documents visibles dépendent du rôle et de l’état d’avancement de la session.

---

## 🧑‍💼 Actions possibles selon le rôle

| Rôle               | Actions possibles                                                                                |
| ------------------ | ------------------------------------------------------------------------------------------------ |
| **Stagiaire**      | S’inscrire à une session disponible                                                              |
| **Formateur**      | Accéder à ses sessions, gérer les présences, remplir les documents pédagogiques                  |
| **Entreprise**     | Inscrire un salarié, consulter les formations suivies par l’équipe                               |
| **Administrateur** | Créer, modifier ou supprimer une session ; consulter tous les participants et documents associés |

---

## 🔐 Sécurité

- Les **actions sensibles** (modification, suppression, inscription) sont toujours protégées par une **modale de confirmation**.
- Les requêtes sont **protégées par un jeton CSRF**.
- Les filtres et recherches sont **validés côté serveur** pour éviter toute manipulation de données non autorisée.

---

## 💡 Astuces

- Les administrateurs peuvent trier les sessions par **date, formateur, type de session ou statut**.
- Un clic sur le **nom du formateur** ouvre une vue détaillée de ses sessions.
- Les filtres actifs restent mémorisés lors de la navigation entre les pages.

---

## ➡️ Pour aller plus loin

👉 **Prochaine section :** [Création de session (Administrateur)](create.md)
