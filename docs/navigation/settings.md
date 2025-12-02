# Paramètres et notifications

## ⚙️ Présentation générale

La section **Paramètres** permet à chaque utilisateur de **personnaliser son expérience** sur la plateforme.  
Accessible depuis le **menu principal** (icône ⚙️ ou “Mon profil”), elle regroupe :

- Informations du compte
- Préférences d’affichage
- Gestion des notifications
- Sécurité et confidentialité

> 💡 Les administrateurs disposent d’options supplémentaires liées à la **configuration globale**.

---

## 👤 Informations du compte

Permet de **modifier ses informations personnelles** :

- Nom et prénom
- Adresse email
- Numéro de téléphone
- Entreprise associée (si applicable)

> Les modifications sont enregistrées **en temps réel** et nécessitent une **validation CSRF**.  
> 🚫 Les champs liés au rôle ou aux permissions ne peuvent pas être modifiés par l’utilisateur.

---

## 🎨 Préférences d’affichage

L’utilisateur peut ajuster :

- **Thème clair / sombre**
- **Langue d’affichage** (si disponible)
- **Nombre d’éléments affichés par page**
- **Affichage en carte ou tableau** selon ses préférences

> Les préférences sont sauvegardées automatiquement dans le navigateur ou le profil utilisateur.

---

## 🔔 Notifications

Les notifications informent l’utilisateur des actions importantes à venir ou à valider.

### Types :

- Nouvelle **inscription à une session**
- **Validation ou refus** d’une demande
- **Documents à remplir** avant ou après formation
- **Mises à jour de compte** ou informations administratives

### Modes d’affichage :

- Icône 🔔 dans l’en-tête
- Liste déroulante des notifications récentes
- Option “Marquer comme lue” pour chaque notification
- ✉️ Certaines notifications peuvent être envoyées par **email automatique**

---

## 🔒 Sécurité et confidentialité

Permet de :

- Modifier son **mot de passe**
- Consulter les **dernières connexions**
- Activer la **double authentification** (si disponible)

Toutes les actions sensibles sont protégées par :

- Une **modale de validation**
- Un **jeton CSRF**

---

## 🧠 Bonnes pratiques

| Thème                | Recommandation                                                          |
| -------------------- | ----------------------------------------------------------------------- |
| Mots de passe        | Utiliser au moins 8 caractères, avec majuscules, chiffres et symboles   |
| Notifications        | Vérifiez-les régulièrement pour ne pas rater une étape de validation    |
| Données personnelles | Maintenez vos informations à jour pour éviter les erreurs d’inscription |

---

## 💡 Astuce

> La section “Paramètres” est accessible depuis **le menu utilisateur en haut à droite**, quel que soit votre rôle.  
> Les préférences sont conservées même après déconnexion.

---

## ➡️ Pour aller plus loin

👉 **Prochaine section :** [Liste des formations](../sessions/list.md)
