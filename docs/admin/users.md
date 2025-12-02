# 👥 Gestion des utilisateurs

Le module **Administration → Utilisateurs** permet aux administrateurs de gérer l’ensemble des comptes présents sur la plateforme : stagiaires, formateurs, financeurs et autres administrateurs.  
C’est un espace central pour le **suivi, la création et la modification** des profils.

---

## 🧭 Accès

- Menu principal : **Administration → Utilisateurs**
- Accessible uniquement aux **administrateurs** disposant du rôle `ROLE_ADMIN`.

---

## 📋 Fonctions principales

| Fonction                                | Description                                                                                                               |
| --------------------------------------- | ------------------------------------------------------------------------------------------------------------------------- |
| 🔍 **Recherche et filtres**             | Permet de retrouver un utilisateur par nom, prénom, email ou rôle.                                                        |
| ➕ **Création de compte**               | L’administrateur peut créer un nouvel utilisateur (stagiaire, formateur, financeur, etc.) directement depuis l’interface. |
| ✏️ **Modification**                     | Possibilité de modifier les informations personnelles, les rôles et le statut d’un utilisateur.                           |
| 🗑️ **Suppression**                      | Supprime un utilisateur après confirmation via une modale.                                                                |
| 🔑 **Réinitialisation de mot de passe** | Envoi d’un email avec lien sécurisé pour réinitialiser le mot de passe.                                                   |

---

## 🧩 Gestion des rôles

Chaque compte possède un ou plusieurs **rôles** déterminant ses permissions.

| Rôle             | Accès principal                                                         |
| ---------------- | ----------------------------------------------------------------------- |
| `ROLE_USER`      | Tableau de bord personnel, inscriptions, documents liés.                |
| `ROLE_FORMATEUR` | Accès aux sessions où il intervient, saisie des évaluations formateurs. |
| `ROLE_FINANCEUR` | Accès aux stagiaires et formations qu’il finance.                       |
| `ROLE_ADMIN`     | Accès complet à toutes les fonctionnalités de l’application.            |

> ⚙️ Lorsqu’un utilisateur est créé, un rôle par défaut (`ROLE_USER`) est attribué automatiquement.

---

## 🧾 Détails d’un utilisateur

En cliquant sur une carte utilisateur, l’administrateur accède à une fiche détaillée comportant :

- Les **informations personnelles** (nom, prénom, email, téléphone)
- Les **formations suivies / animées**
- Le **statut d’inscription**
- Les **documents liés**
- Les **actions rapides** :
  - Modifier
  - Réinitialiser le mot de passe
  - Supprimer

<pre>
+------------------------------------------------------------+
| 👤 Jean Dupont (ROLE_USER)                                 |
| Email : jean.dupont@email.com                              |
| Téléphone : 06 00 00 00 00                                 |
| Formations suivies : Excel – Niveau 2, Word Initiation     |
|                                                            |
| Actions : [Modifier] [Réinitialiser mot de passe] [Suppr.] |
+------------------------------------------------------------+
</pre>

---

## 🔐 Sécurité et validation

- Toute suppression nécessite une **confirmation via modale**.
- Les formulaires de création/modification sont protégés par un **token CSRF**.
- Les mots de passe sont **hashés** avant stockage (BCrypt).
- L’email de réinitialisation contient un **code PIN unique** à usage unique.

---

## 📈 Bonnes pratiques

- Vérifier les **rôles** avant chaque modification.
- Éviter de supprimer un utilisateur lié à des inscriptions en cours (préférer la **désactivation**).
- Utiliser les filtres pour un suivi rapide par rôle ou statut.

---

## 🧰 Astuce

> Pour les grandes structures, l’import de comptes par **fichier CSV** peut être activé sur demande (optionnel selon le déploiement).

---

👉 **Prochaine section :** [Gestion des sessions](sessions.md)
