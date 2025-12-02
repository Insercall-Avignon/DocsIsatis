# Présentation générale

## 🧭 Contexte du projet

L’application **Isatis Formation** est une plateforme web interne conçue pour simplifier et automatiser la **gestion complète du processus de formation professionnelle**.  
Elle centralise l’ensemble des actions liées aux utilisateurs, aux sessions de formation, aux inscriptions, aux documents et aux évaluations.

Cette solution a été développée pour **faciliter le travail administratif**, **améliorer le suivi des apprenants** et **renforcer la communication** entre les différents acteurs de la formation.

---

## 🎯 Objectifs principaux

- Simplifier la gestion des **sessions de formation** et des participants.  
- Permettre le **suivi complet du parcours des stagiaires**, depuis l’inscription jusqu’à l’attestation.  
- Centraliser les **documents administratifs et pédagogiques** liés à chaque session.  
- Favoriser la **collaboration entre administrateurs, formateurs et entreprises clientes**.  
- Assurer la **sécurité, la traçabilité et la conformité** des données.  

---

## 👥 Profils utilisateurs

L’application distingue plusieurs types d’utilisateurs, chacun ayant des droits et fonctionnalités adaptés à son rôle :

| Profil | Description |
| ------ | ------------ |
| **Administrateur** | Supervise la plateforme, gère les utilisateurs, les sessions, les inscriptions et les documents. |
| **Formateur** | Consulte et gère ses propres sessions, dépose les supports pédagogiques et suit ses apprenants. |
| **Stagiaire (apprenant)** | Accède à ses formations, complète les évaluations et télécharge ses documents. |
| **Entreprise / Client** | Suit les formations de ses employés et récupère les documents administratifs associés. |

---

## 🧩 Modules fonctionnels

L’application est structurée autour de plusieurs modules principaux :

1. **Authentification et gestion du compte**  
   Connexion sécurisée, réinitialisation du mot de passe, et mise à jour des informations personnelles.

2. **Formations et sessions**  
   Création, gestion et suivi des sessions de formation.  
   Invitation et inscription des participants, selon leur rôle.

3. **Documents**  
   Accès et édition des documents liés à une session.  
   Certains documents sont générés automatiquement au fil du processus.

4. **Évaluations**  
   Questionnaires de positionnement, de connaissance ou de satisfaction, selon les étapes de la formation.

5. **Administration**  
   Accès réservé à l’administrateur pour superviser l’ensemble des données : utilisateurs, sessions, statistiques et paramétrages globaux.

---

## 🔐 Sécurité et accessibilité

- Chaque ressource est **protégée par des rôles utilisateurs**.  
- Les formulaires sont sécurisés par des **jetons CSRF**.  
- Les actions importantes (suppression, validation, envoi de mail, etc.) nécessitent une **confirmation explicite**.  
- L’application est **responsive**, compatible avec ordinateurs, tablettes et smartphones.

---

## 📄 Pour aller plus loin

👉 **Prochaine section :** [Accès à l’application](access.md)
