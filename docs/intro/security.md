# Sécurité et responsivité

## 🔒 Sécurité de l’application

L’application **Isatis Formation** applique une politique de sécurité complète : authentification robuste, contrôle d’accès selon les rôles et traçabilité des actions.

---

### 🔸 Authentification et gestion de session

- Connexion sécurisée avec e-mail et mot de passe.
- Les mots de passe sont **toujours protégés**.
- Fonctionnalité **“Se souvenir de moi”** pour prolonger la session sur un appareil de confiance.
- Les sessions expirent automatiquement après une période d’inactivité.
- Déconnexion simple et sécurisée.

> ✅ Les liens de réinitialisation de mot de passe sont temporaires et à usage unique.

---

### 🔸 Gestion des rôles et des accès

Chaque utilisateur dispose d’un rôle qui détermine ce qu’il peut consulter ou modifier :

| Rôle                      | Accès principal                                                    |
| ------------------------- | ------------------------------------------------------------------ |
| **Administrateur**        | Accès complet à la plateforme (utilisateurs, sessions, documents). |
| **Formateur**             | Accès à ses propres sessions et participants.                      |
| **Stagiaire (apprenant)** | Accès à ses inscriptions, évaluations et documents.                |
| **Entreprise / Client**   | Accès aux sessions et documents liés à ses employés.               |

---

### 🔸 Actions sensibles et confirmations

Toutes les opérations critiques (modification, suppression, validation) demandent **une confirmation** avant exécution.

> 🧠 Cela évite les erreurs et assure la traçabilité des actions importantes.

---

### 🔸 Traçabilité

Certaines actions peuvent être enregistrées afin de :

- Conserver un **historique des modifications**
- Identifier l’utilisateur à l’origine d’une action
- Faciliter le support et les audits

> 🔐 Aucune information sensible comme les mots de passe n’est stockée dans ces journaux.

---

## 📱 Responsivité de l’interface

L’application est conçue pour une **utilisation fluide sur tous les supports** :

- 💻 Ordinateur de bureau
- 📱 Smartphone
- 📟 Tablette

> L’interface s’adapte automatiquement à la taille de l’écran, sans perte de fonctionnalité.

---

## ➡️ Pour aller plus loin

👉 **Prochaine section :** [Connexion et mot de passe](../users/auth.md)
