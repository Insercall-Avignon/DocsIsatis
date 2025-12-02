# Documentation Utilisateur – Application Isatis Formation

Bienvenue dans la documentation utilisateur de l’application **Isatis Formation**.  
Cette application web permet de **gérer l’ensemble du processus de formation** : de l’inscription des stagiaires jusqu’au suivi administratif et aux évaluations.

---

## 🎯 Objectif de l’application

L’application vise à centraliser toutes les informations liées aux formations :

- Gestion des **utilisateurs** (stagiaires, formateurs, entreprises, administrateurs)
- Création et suivi des **sessions de formation**
- Gestion des **documents administratifs** (convocations, attestations, feuilles d’émargement, questionnaires…)
- Réalisation des **évaluations** avant, pendant et après les formations
- Consultation des **statistiques et rapports**

---

## 👥 Profils utilisateurs

L’application prend en charge plusieurs types d’utilisateurs, chacun disposant d’un espace et de droits spécifiques :

| Rôle                      | Description                                                                    |
| ------------------------- | ------------------------------------------------------------------------------ |
| **Administrateur**        | Gère les utilisateurs, sessions, documents et statistiques globales.           |
| **Formateur**             | Accède à ses sessions, consulte les inscrits et dépose des documents.          |
| **Stagiaire (apprenant)** | Consulte ses formations, complète ses évaluations et télécharge ses documents. |
| **Entreprise / Client**   | Suit les sessions et salariés formés, accède aux documents correspondants.     |

---

## 💡 Points clés techniques

- **Interface responsive** : adaptée aux ordinateurs, tablettes et mobiles.
- **Sécurité** : formulaires protégés par **tokens CSRF**, accès contrôlé selon les rôles.
- **Formulaires dynamiques** : affichage et validation des champs en temps réel.
- **Système de modales** : confirmation avant toute action critique (suppression, modification importante).

---

## 🚀 Structure de la documentation

La documentation est organisée par modules :

1. **Introduction** – Présentation générale et sécurité
2. **Utilisateurs** – Connexion, gestion de compte et rôles
3. **Navigation générale** – Tableau de bord, listes et paramètres
4. **Formations et sessions** – Inscription et suivi des formations
5. **Documents** – Types, accès et génération automatique
6. **Évaluations** – Questionnaires et retours
7. **Administration** – Gestion avancée et statistiques
8. **Annexes** – Schéma fonctionnel, lexique, FAQ, contact

---

## 📚 À propos

- Projet développé avec **Symfony (backend)** et avec le moteur de template **Twig (frontend)**
- Documentation générée avec **MkDocs**
- Dernière mise à jour : **3 novembre 2025**
