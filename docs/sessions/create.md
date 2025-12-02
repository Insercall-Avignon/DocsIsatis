# Création de session (Administrateur)

## 🎯 Objectif

La page **Création de session** permet aux administrateurs d’ajouter de nouvelles sessions de formation, de définir leurs paramètres principaux (dates, formateur, lieu, nombre de places, type de session) et d’inviter des participants.  
C’est un point central pour gérer les formations sur **Isatis Formation**.

---

## 🧭 Accès

- Réservé aux **administrateurs** et aux **formateurs responsables** disposant des droits de gestion.
- Accessible depuis :
  - Le **tableau de bord administrateur**
  - La **liste des sessions** via le bouton ➕ “Créer une session”

---

## 🧾 Structure du formulaire

Le formulaire de création est **dynamique** et comporte plusieurs sections principales :

### 1️⃣ Informations générales

- **Nom de la formation** (sélection ou saisie)
- **Dates de début et de fin**
- **Durée totale** : ex. **2 semaines**
- **Type de session** : **INTRA** (réservée à une entreprise) ou **INTER** (ouverte à plusieurs participants)
- **Lieu de formation**
- **Mode** : Présentiel / Distanciel / Hybride
- **Formateur principal**
- **Nombre de places disponibles**
- **Statut initial** : Ouverte / Brouillon / Privée

### 2️⃣ Détails pédagogiques

- **Objectifs** (texte libre)
- **Programme** (texte ou document attaché)
- **Durée totale (heures ou jours)**

### 3️⃣ Configuration administrative

- **Documents requis** (convocation, feuille d’émargement, etc.)

---

## ⚙️ Comportement dynamique

Le formulaire **s’adapte automatiquement** selon les choix effectués :

- Si le mode “Distanciel” est choisi → affichage du lien de connexion et consignes techniques
- Si un formateur est sélectionné → affichage automatique de son profil résumé
- Si le type de session est **INTRA** → affichage de champs supplémentaires pour l’entreprise
- Si le type de session est **INTER** → affichage des champs pour inscription ouverte à plusieurs participants

> 💡 Tout se fait automatiquement, sans intervention technique de votre part.

---

## 📤 Validation et enregistrement

- Les champs obligatoires sont **vérifiés en temps réel**
- Une **modale de confirmation** apparaît avant l’enregistrement
- Une fois la session créée, elle apparaît automatiquement dans la **liste des formations**

---

## ✉️ Invitations et inscriptions

Après création :

1. L’administrateur peut **inviter des participants** depuis la page de session
2. Les invitations sont envoyées **par email**
3. Chaque participant doit **confirmer sa participation**
4. Si le participant n’a pas de compte, il est invité à **créer son compte automatiquement**

---

## 🧑‍💼 Actions possibles

| Action                | Rôle autorisé                          | Description                                           |
| --------------------- | -------------------------------------- | ----------------------------------------------------- |
| Créer une session     | Administrateur                         | Depuis le tableau de bord                             |
| Modifier une session  | Administrateur / Formateur responsable | Mettre à jour les informations                        |
| Supprimer une session | Administrateur                         | Suppression définitive avec confirmation              |
| Dupliquer une session | Administrateur                         | Reprendre une session existante pour un nouveau cycle |

---

## 🔐 Sécurité

- Accès restreint aux **rôles autorisés**
- Toutes les actions sensibles sont protégées par **CSRF** et confirmation
- Les modifications sont **journalisées** pour un suivi interne

---

## 💡 Bonnes pratiques

- Utiliser des **noms clairs et datés** pour les sessions (ex : _“Excel – Niveau Intermédiaire – Mars 2025”_)
- Vérifier le **nombre de places disponibles**
- Indiquer correctement le **type de session** (**INTRA / INTER**) et la **durée** (ex. 2 semaines)
- Utiliser la **duplication** pour créer rapidement des sessions récurrentes

---

## ➡️ Pour aller plus loin

👉 **Prochaine section :** [Participation à une session](registration.md)
