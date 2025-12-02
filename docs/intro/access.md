# Accès à l’application

## 🌐 URL d’accès

L’application **Isatis Formation** est accessible depuis n’importe quel navigateur web moderne (Chrome, Firefox, Edge, Safari).

> ⚠️ Une connexion Internet est nécessaire.  
> L’adresse exacte dépend de votre environnement d’hébergement (exemple : `https://isatis-formation.fr` ou une URL interne).

---

## 🔐 Page de connexion

La page de connexion permet à tout utilisateur disposant d’un compte actif d’accéder à l’application.  
Elle comprend :

- Un champ **Adresse e-mail**
- Un champ **Mot de passe**
- Une **icône “œil”** pour afficher ou masquer le mot de passe saisi
- Une case **Se souvenir de moi** (selon les préférences du navigateur)
- Un lien **« Mot de passe oublié ? »** pour accéder à la procédure de réinitialisation

> En cas de connexion réussie, l’utilisateur est automatiquement redirigé vers son **tableau de bord**.

---

## 🔄 Réinitialisation du mot de passe

En cas d’oubli, il est possible de réinitialiser le mot de passe directement depuis la page de connexion :

1. Cliquer sur **« Mot de passe oublié ? »**
2. Une fenêtre s’ouvre (modale) permettant de saisir **votre adresse e-mail**
3. Vous recevrez ensuite un lien sécurisé pour définir un **nouveau mot de passe**

> 🟢 Cette procédure est entièrement intégrée à l’application et s’effectue via une interface simple et sécurisée.  
> Le lien de réinitialisation est **valide pour une durée limitée** et ne peut être utilisé qu’une seule fois.

---

## 👥 Création et gestion des comptes

### 1. Création d’un compte

Un compte peut être créé :

- **par l’utilisateur lui-même** lors d’une première inscription,
- **ou par un administrateur**, lors d’une invitation à une session ou d’une création manuelle.

Les informations de base à renseigner sont :

- Nom et prénom
- Adresse e-mail
- Mot de passe sécurisé
- Rôle ou profil utilisateur (selon le contexte)

---

### 2. Gestion des comptes selon les rôles

| Rôle                      | Droits d’accès principaux                                                |
| ------------------------- | ------------------------------------------------------------------------ |
| **Administrateur**        | Peut créer, modifier ou supprimer n’importe quel compte utilisateur.     |
| **Formateur**             | Peut consulter ses sessions et gérer les utilisateurs qui y participent. |
| **Stagiaire (Apprenant)** | Peut modifier ses informations personnelles, mais pas son rôle.          |
| **Entreprise / Client**   | Suit les sessions de ses employés et récupère les documents associés.    |

Les administrateurs disposent d’un **accès complet** à la gestion des comptes, tandis que les autres rôles ne peuvent consulter ou modifier que leurs propres données.

---

## 🔒 Sécurisation des accès

- Chaque ressource est **protégée en fonction du rôle utilisateur**.
- Les formulaires sont sécurisés par un **jeton CSRF** pour éviter toute attaque.
- Les actions sensibles (modification, suppression, validation) affichent une **modale de confirmation** avant exécution.
- Les sessions expirent automatiquement après une période d’inactivité prolongée.

---

## 📱 Responsivité

L’application est entièrement **responsive**, garantissant une expérience fluide sur tous les supports :

- 💻 Ordinateur de bureau
- 📱 Smartphone
- 📟 Tablette

L’interface s’adapte automatiquement à la taille de l’écran, sans perte de fonctionnalité.

---

## ➡️ Pour aller plus loin

👉 **Prochaine section :** [Sécurité et responsivité](security.md)
