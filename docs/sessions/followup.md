# Suivi des inscriptions

## 🎯 Objectif

Le **suivi des inscriptions** permet de visualiser et gérer l’ensemble des inscriptions à une session de formation.  
Cette page centralise les **statuts des participants**, les **documents associés**, et les **actions de gestion** disponibles selon le rôle de l’utilisateur.

> 💡 Certaines informations contextuelles, comme le **type de session (INTRA/INTER)** et la **durée indicative (ex. 2 semaines)**, sont affichées dans les détails pour faciliter la lecture et la planification.

---

## 🧭 Accès

L’accès varie selon le rôle :

| Rôle           | Accès                                                            |
| -------------- | ---------------------------------------------------------------- |
| Stagiaire      | Peut consulter uniquement ses propres inscriptions               |
| Formateur      | Peut consulter la liste des stagiaires inscrits à ses sessions   |
| Administrateur | Dispose d’un accès complet à toutes les sessions et inscriptions |

> 💡 Les administrateurs peuvent également **filtrer** les inscriptions par formation, par date, par statut, et par **type de session** (INTRA / INTER).

---

## 🗂️ Présentation générale

Le tableau de suivi se compose de plusieurs **cartes ou lignes**, selon le mode d’affichage choisi (liste ou cartes).

Chaque carte d’inscription contient :

- Le **nom du stagiaire**
- Le **titre de la formation**
- Le **type de session** (INTRA / INTER)
- La **durée** (ex. 2 semaines)
- Le **statut actuel** (En attente, Validée, Refusée, En cours, Terminée)
- Les **dates de session**
- Des **raccourcis** vers les documents associés ou les actions de gestion

---

## 🧾 Statuts d’inscription

| Statut        | Description                                                           |
| ------------- | --------------------------------------------------------------------- |
| 🕓 En attente | La demande est soumise, en attente de validation par l’administration |
| ✅ Acceptée   | La participation du stagiaire est confirmée                           |
| 🚫 Refusée    | La demande a été refusée (raison précisée si applicable)              |
| 🎓 En cours   | La formation est actuellement en déroulement                          |
| 📄 Terminée   | La formation est achevée, les documents de fin sont disponibles       |

> 📢 Certains statuts déclenchent automatiquement des **notifications par email** (acceptation, refus, fin de formation).

---

## 🔍 Fonctions principales

### 🔎 Recherche et filtres

Le système de recherche permet de retrouver rapidement une inscription selon :

- le nom du stagiaire
- le titre de la formation
- le statut
- la date de session
- le **type de session** (INTRA / INTER)

Les **filtres combinés** (statut + formation + date + type) offrent une navigation fluide dans un grand volume de données.

### 🧮 Tri et pagination

- Les inscriptions peuvent être triées par **nom**, **date**, **statut**, ou **type de session**.
- Un système de **pagination** évite la surcharge du navigateur.

---

## 🧰 Actions disponibles

| Action                      | Rôle autorisé         | Description                                          |
| --------------------------- | --------------------- | ---------------------------------------------------- |
| Modifier une inscription    | Administrateur        | Mise à jour des informations administratives         |
| Changer le statut           | Administrateur        | Validation ou refus de la demande                    |
| Supprimer une inscription   | Administrateur        | Suppression définitive (avec modale de confirmation) |
| Consulter les documents     | Tous                  | Accès aux documents liés à la formation              |
| Télécharger un justificatif | Formateur / Stagiaire | Export PDF ou feuille d’émargement                   |

> ⚙️ Les actions sensibles déclenchent une **modale de confirmation** pour éviter toute suppression accidentelle.

---

## 📄 Raccourcis et documents

Chaque inscription peut donner accès à différents **documents dynamiques**, en fonction du statut et du rôle :

- **Avant la formation :**

  - Convocation
  - Convention de formation
  - Questionnaire préformation

- **Pendant la formation :**

  - Feuille d’émargement (en ligne ou à imprimer)
  - QCM ou questionnaire d’évaluation

- **Après la formation :**
  - Attestation de présence
  - Évaluation de satisfaction (formulaire à chaud)
  - Compte-rendu de session

Les raccourcis s’affichent automatiquement sur chaque carte d’inscription.

---

## 🧩 Suivi dynamique

Le tableau se **met à jour en temps réel** après chaque action :

- Validation, refus ou suppression d’une inscription.
- Mise à jour d’un document ou d’un statut.

Ce comportement est géré côté **front Twig + JavaScript**, via des appels AJAX sécurisés.

---

## 🔐 Sécurité et permissions

- Toutes les actions sont **protégées par des jetons CSRF**.
- Les rôles et permissions sont gérés via le **système de sécurité Symfony**.
- L’accès est restreint aux inscriptions que l’utilisateur est autorisé à consulter.

> 🛡️ Les logs enregistrent toute modification ou validation d’inscription effectuée par un administrateur.

---

## 📊 Exemple visuel (résumé d’écran)

<pre>
+------------------------------------------------------------+
| [Excel – Niveau 2 – Mars 2025]                             |
| Type de session : INTER                                    |
| Durée : 2 semaines                                         |
| Stagiaire : Jean Dupont                                    |
| Status    : Acceptée                                       |
| Documents : [Convocation] [Feuille émargement] [QCM]       |
| Actions   : [Modifier] [Supprimer] [Voir session]          |
+------------------------------------------------------------+
</pre>

---

## 💡 Bonnes pratiques

- Vérifiez le **statut** de chaque inscription avant de transmettre les documents.
- Utilisez les **filtres** pour trier efficacement les inscriptions par session ou statut.
- Ne supprimez jamais une inscription sans confirmation explicite du stagiaire.

---

## ➡️ Pour aller plus loin

👉 **Prochaine section :** [Types de documents](../documents/types.md)
