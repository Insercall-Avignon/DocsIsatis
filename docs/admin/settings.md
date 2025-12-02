# ⚙️ Paramétrage général de l’application

Le module **Administration → Paramètres** permet aux administrateurs de configurer les éléments essentiels de l’application : identité de l’organisme, messages automatiques, modèles de documents, gestion des rôles, etc.  
Il garantit le bon fonctionnement et la personnalisation du portail Isatis Formation.

---

## 🧭 Accès

- Menu : **Administration → Paramètres**
- Accessible uniquement aux **administrateurs principaux** (`ROLE_ADMIN`).
- Interface structurée par **onglets** pour un accès rapide à chaque catégorie de configuration.

---

## 🧩 Catégories de paramètres

| Catégorie                      | Description                                                                                                  |
| ------------------------------ | ------------------------------------------------------------------------------------------------------------ |
| 🏢 **Informations générales**  | Nom de l’organisme, logo, coordonnées, mentions légales.                                                     |
| ✉️ **Notifications & e-mails** | Personnalisation des messages envoyés (inscription, confirmation, rappel, etc.).                             |
| 📄 **Modèles de documents**    | Gestion des modèles Twig pour la génération automatique (convocations, attestations, feuilles d’émargement). |
| 🔐 **Sécurité & rôles**        | Gestion des rôles utilisateurs et paramètres d’authentification.                                             |
| 🕓 **Calendrier & délais**     | Paramétrage des rappels automatiques et relances d’évaluations.                                              |

---

## 🏢 Informations générales

L’administrateur peut définir les éléments d’identité de l’organisme :

- **Nom** : “Isatis Formation”
- **Logo** : image affichée sur les documents et l’interface
- **Adresse / contact**
- **Mentions légales**
- **Pied de page** des documents générés automatiquement

Ces informations se répercutent automatiquement dans tous les modèles de documents.

---

## ✉️ Notifications & e-mails automatiques

L’administrateur peut personnaliser les e-mails automatiques envoyés depuis l’application :

| Type de message              | Moment d’envoi          | Contenu personnalisable            |
| ---------------------------- | ----------------------- | ---------------------------------- |
| Confirmation d’inscription   | Après validation admin  | Message de bienvenue               |
| Convocation                  | Avant la formation      | Détails pratiques (dates, lieu)    |
| Rappel de satisfaction       | Après la formation      | Lien vers le questionnaire à chaud |
| Relance satisfaction à froid | 3 mois après la session | Lien vers le second questionnaire  |

> 🧠 Astuce : des variables dynamiques comme `{{ user.firstname }}` ou `{{ session.title }}` peuvent être intégrées pour personnaliser chaque e-mail.

---

## 📄 Modèles de documents (Twig)

Les documents générés automatiquement utilisent des **modèles Twig** stockés côté serveur.  
L’administrateur peut :

- Modifier le contenu et la mise en page,
- Ajouter des **variables dynamiques** (nom, dates, formateur, lieu),
- Tester la génération avant mise en ligne,
- Restaurer un modèle par défaut.

> 🧩 Exemple de variable Twig :  
> `{{ session.trainer.name }}` → affiche le nom du formateur de la session.

---

## 🔐 Sécurité et gestion des rôles

L’administrateur peut :

- Ajouter ou supprimer des **rôles personnalisés** (ex : `ROLE_FINANCEUR`),
- Modifier les **permissions d’accès** par module,
- Configurer la **politique de mot de passe** (longueur minimale, caractères spéciaux),
- Activer la **double authentification** (optionnelle).

Toutes les modifications sont immédiatement prises en compte.

---

## 🕓 Calendrier & automatisations

Paramètres liés à la planification :

- Délais avant relance automatique des stagiaires non répondants (par défaut : 7 jours),
- Durée avant envoi des évaluations à froid (par défaut : 90 jours après la session),
- Périodes d’archivage automatique des sessions terminées.

---

## 📤 Sauvegarde et restauration

Chaque ensemble de paramètres peut être :

- **Exporté** au format `.json` pour sauvegarde,
- **Importé** pour restaurer une configuration précédente.

> 🔒 Seul un administrateur principal peut exécuter cette action.

---

## 💡 Bonnes pratiques

- Sauvegarder la configuration après chaque mise à jour importante.
- Tester les modèles de documents sur une **session fictive** avant déploiement réel.
- Centraliser toutes les communications officielles dans la section _Notifications_.
- Garder une cohérence visuelle (logo, couleurs, mentions).

---

👉 **Prochaine section :** [Schéma fonctionnel](../annexes/arborescence.md)
