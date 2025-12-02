# Participation à une session

## 🎯 Objectif

Cette section décrit le fonctionnement du **système d’inscription à une session de formation**, qu’il s’agisse :

- d’une **invitation envoyée par un administrateur**, ou
- d’une **demande directe** faite par un utilisateur (stagiaire).

---

## 🧭 Accès

L’inscription peut être initiée de deux manières :

1. **Depuis un administrateur :**

   - L’admin sélectionne une session existante.
   - Il invite des personnes à y participer via le formulaire d’ajout de participants.
   - Chaque invité reçoit un **email de confirmation** contenant un lien d’inscription sécurisé.

2. **Depuis un stagiaire (auto-inscription) :**
   - L’utilisateur, connecté ou non, accède à la page publique d’une session.
   - Il clique sur “Demander une participation”.
   - Une vérification d’identité est effectuée (connexion requise ou création de compte).

---

## 🧩 Étapes du processus

### 1️⃣ Vérification de l’identité

- Si l’utilisateur n’est **pas connecté**, il est redirigé vers la **page de connexion ou d’inscription**.
- Une fois authentifié, le système vérifie :
  - S’il a déjà une inscription en cours sur cette session.
  - Si des restrictions de rôle ou de quota s’appliquent.

### 2️⃣ Sélection des informations administratives

Le formulaire permet de renseigner :

- **Employeur** du salarié (peut être l’utilisateur lui-même)
- **Financeur** (ex : entreprise, OPCO, Pôle Emploi)
- **Statut professionnel**
- **Commentaires** éventuels

Le formulaire est **dynamique** :

- Si le financeur choisi est “Autre”, un champ libre apparaît pour la précision.
- Si l’utilisateur est lui-même le financeur ou l’employeur, les champs se remplissent automatiquement.

> 🧠 Objectif : simplifier au maximum la saisie tout en conservant les données administratives nécessaires.

---

### 3️⃣ Validation et confirmation

Une fois la demande complétée :

- L’utilisateur valide via une **modale de confirmation**.
- Un **jeton CSRF** sécurise la requête.
- Une **notification est envoyée à l’administrateur**, qui doit approuver ou refuser la demande.

> ✅ L’utilisateur reçoit également un **email de confirmation** de dépôt de demande.

---

### 4️⃣ Vérification administrative

Côté **administration**, la demande apparaît dans la liste des inscriptions en attente.

L’administrateur peut :

- **Accepter** la demande → la session devient active pour ce stagiaire.
- **Refuser** la demande → l’utilisateur reçoit un message indiquant le refus et les motifs éventuels.

Chaque inscription validée fusionne les données :

- du **stagiaire**
- de la **session**
- et des **éléments administratifs** (statut, dates, documents associés).

---

## 🧾 Données enregistrées

| Champ            | Description                                       |
| ---------------- | ------------------------------------------------- |
| Session          | Identifiant de la session choisie                 |
| Utilisateur      | Stagiaire concerné                                |
| Employeur        | Société ou individu financeur                     |
| Statut           | En attente / Acceptée / Refusée                   |
| Date de demande  | Date de création de l’inscription                 |
| Validation admin | Booléen, mis à jour lors de la décision           |
| Documents liés   | Liste des fichiers à compléter selon l’avancement |

---

## 🔐 Sécurité

- Chaque étape est protégée par un **jeton CSRF**.
- Les inscriptions ne peuvent être modifiées qu’avant validation finale.
- L’accès au formulaire dépend :
  - du **statut de la session** (ouverte ou fermée)
  - et du **rôle utilisateur**.

> 💬 Les administrateurs peuvent à tout moment **annuler une inscription** pour motif administratif.

---

## 📧 Notifications automatiques

| Événement                   | Destinataire          | Contenu                                          |
| --------------------------- | --------------------- | ------------------------------------------------ |
| Demande d’inscription       | Administrateur        | Notification d’une nouvelle demande              |
| Validation de l’inscription | Stagiaire             | Confirmation d’inscription + lien vers documents |
| Refus d’inscription         | Stagiaire             | Message d’explication                            |
| Modification de session     | Tous les participants | Notification du changement de date ou de lieu    |

---

## 🧭 Exemple de parcours utilisateur

1. Un stagiaire consulte la session _“Excel Intermédiaire – Mars 2025”_.
2. Il clique sur **S’inscrire**.
3. Il se connecte (ou crée un compte).
4. Il choisit son financeur et valide la demande.
5. L’administrateur reçoit une notification et valide.
6. L’utilisateur accède alors aux **documents liés à son inscription**.

---

## 💡 Bonnes pratiques

- Vérifiez toujours vos **informations employeur/financeur** avant validation.
- Consultez votre **tableau de bord** pour suivre le statut de vos demandes.
- En cas d’erreur, contactez un **administrateur** avant validation finale.

---

## ➡️ Pour aller plus loin

👉 **Prochaine section :** [Suivi des inscriptions](followup.md)
