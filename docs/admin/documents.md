# 📂 Gestion des documents

Le module **Administration → Documents** permet de gérer tous les fichiers liés aux formations : documents administratifs, pédagogiques ou d’évaluation.  
Il s’agit d’un espace centralisé où les administrateurs peuvent **ajouter, modifier, télécharger ou valider** les documents associés à chaque session.

---

## 🧭 Accès

- Menu : **Administration → Documents**  
- Accessible uniquement aux utilisateurs disposant du rôle `ROLE_ADMIN`.  
- Vue par **liste ou carte**, regroupant les documents par session ou par type.

---

## 📋 Types de documents gérés

| Catégorie | Exemples | Accès |
|------------|-----------|-------|
| 🧾 **Administratifs** | Convocation, Feuille d’émargement, Attestation de présence | Admin, Formateur |
| 📘 **Pédagogiques** | Support de formation, QCM, Exercices | Formateur, Stagiaire |
| 🧠 **Évaluations** | Questionnaire de connaissance, Feedback à chaud/froid | Stagiaire, Admin |

> Certains documents apparaissent automatiquement à mesure que la session avance (ex. le QCM pendant la formation, le feedback après).

---

## ⚙️ Fonctions principales

| Fonction | Description |
|-----------|--------------|
| ➕ **Ajout de document** | L’administrateur peut téléverser un fichier PDF, DOCX ou image lié à une session. |
| ✏️ **Édition des métadonnées** | Modification du titre, description, type et visibilité du document. |
| 🔄 **Mise à jour automatique** | Les documents peuvent être régénérés selon des modèles Twig préconfigurés. |
| 🔍 **Filtrage et recherche** | Filtrer par session, formateur, type ou statut. |
| 🗑️ **Suppression sécurisée** | Confirmation obligatoire avant suppression. |

---

## 📑 Détails d’un document

Chaque carte de document affiche :

| Élément | Description |
|----------|--------------|
| **Nom** | Titre du document (ex. “Convocation – Excel Niveau 2”) |
| **Type** | Catégorie : administratif, pédagogique, évaluation |
| **Session liée** | Lien vers la formation concernée |
| **Statut** | Généré / En attente / Validé |
| **Visibilité** | Restreinte selon le rôle de l’utilisateur |
| **Actions** | Télécharger / Modifier / Supprimer |

<pre>
+------------------------------------------------------------+
| 📄 Convocation – Excel Niveau 2                             |
| Session : Mars 2025                                         |
| Type : Administratif                                        |
| Statut : ✅ Validé                                           |
| Visibilité : Formateur, Stagiaires inscrits                 |
|                                                            |
| [⬇️ Télécharger] [✏️ Modifier] [🗑️ Supprimer]                |
+------------------------------------------------------------+
</pre>

---

## 🧠 Génération automatique

Certains documents sont **générés automatiquement** à partir de modèles Twig :

| Document | Déclencheur | Contenu généré |
|-----------|-------------|----------------|
| Convocation | Validation d’inscription | Nom du stagiaire, dates, lieu |
| Feuille d’émargement | Début de la session | Liste des participants |
| Attestation de présence | Clôture de la session | Identité + durée de présence |
| QCM / Feedback | Selon calendrier | Questionnaire associé à la session |

> 🧩 Les modèles Twig sont dynamiques : ils intègrent les données de la session et du participant en temps réel.

---

## 🔒 Sécurité et contrôle d’accès

- Chaque document est associé à un **rôle d’accès** (admin, stagiaire, formateur, financeur).  
- Les téléchargements sont soumis à **authentification**.  
- Les fichiers sont stockés sur un serveur sécurisé, avec **contrôle des droits Symfony**.  
- Les suppressions sont irréversibles et nécessitent une **confirmation explicite**.

---

## 📈 Bonnes pratiques

- Toujours **valider les documents générés automatiquement** avant diffusion.  
- Supprimer les doublons ou fichiers obsolètes pour alléger le stockage.  
- Favoriser les **formats PDF** pour la compatibilité inter-plateformes.  
- Utiliser des noms clairs : `Convocation_Excel_Mars2025.pdf`.

---

👉 **Prochaine section :** [Statistiques et rapports](stats.md)
