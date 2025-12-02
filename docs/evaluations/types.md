# 🧠 Types de questionnaires et évaluations

L’application **Isatis Formation** intègre plusieurs types de questionnaires permettant d’évaluer à la fois :

- les **connaissances** des stagiaires,
- la **satisfaction** des différents acteurs (stagiaires, formateurs, employeurs, financeurs),
- et la **qualité globale** des formations organisées.

Chaque évaluation est rattachée à une **inscription** ou une **session** et gérée automatiquement selon le rôle de l’utilisateur.

---

## 📋 Catégories principales

### 1. Évaluations de connaissances

Basées sur l’entité `Knowledge`, elles permettent de mesurer la progression du stagiaire.

- **Questionnaire préformation** : évalue le niveau initial du stagiaire avant la session.  
- **QCM ou test intermédiaire** : permet au formateur de suivre la progression en cours de formation.  
- **Évaluation finale** : valide les acquis et les compétences à la fin de la formation.

> 🧩 Ces questionnaires sont liés directement à l’**inscription** (`Inscription`) et enregistrés en base via les réponses associées.

---

### 2. Évaluations de satisfaction

Ces grilles recueillent le **retour qualitatif** des différents participants à la formation.

| Rôle concerné | Type de retour | Accès via |
| -------------- | -------------- | ---------- |
| 🧍‍♂️ **Stagiaire** | Questionnaire de satisfaction (contenu, formateur, logistique) | `/inscription/{id}/feedback/trainee` |
| 👨‍🏫 **Formateur** | Retour pédagogique sur le déroulement de la session | `/session/{id}/feedback/former` |
| 🏢 **Employeur** | Évaluation de la pertinence et du bénéfice de la formation | `/inscription/{id}/feedback/employer` |
| 💶 **Financeur** | Retour administratif et satisfaction globale du dispositif | `/inscription/{id}/feedback/financer` |

Chaque questionnaire est rempli en ligne et ensuite **généré automatiquement en PDF** pour archivage.

---

## 🧩 Fonctionnement général

- Les questionnaires sont accessibles depuis la **fiche session** ou **fiche inscription**.  
- Les réponses sont **enregistrées automatiquement** en base de données.  
- Une fois validé, le formulaire devient **verrouillé** (non modifiable).  
- L’administrateur peut consulter et télécharger toutes les grilles (PDF).

---

## 🧾 Génération des PDF

Chaque retour d’évaluation est exporté en **PDF** grâce au système interne de génération (`pdf.html.twig`).  
Le fichier contient :

- le contenu intégral des questions et réponses,  
- le nom du participant,  
- les dates et informations de la session.

Les fichiers sont sécurisés et **téléchargeables uniquement par les rôles autorisés**.

---

## 📅 Disponibilité selon le moment de la session

| Moment de la session | Évaluation concernée | Rôle associé |
| --------------------- | -------------------- | ------------- |
| **Avant la formation** | Questionnaire préformation | Stagiaire |
| **Pendant la formation** | QCM, Évaluation intermédiaire | Stagiaire / Formateur |
| **Après la formation** | Questionnaire de satisfaction | Stagiaire / Formateur / Employeur / Financeur |

---

## 📊 Exemple d’écran

<pre>
+------------------------------------------------------------+
| Questionnaire de satisfaction – Stagiaire                  |
| Session : Excel – Niveau 2 – Mars 2025                     |
|                                                            |___
| 1️⃣ Le contenu correspondait à mes attentes.      ⭐⭐⭐⭐☆   |
| 2️⃣ Le formateur était clair et disponible.       ⭐⭐⭐⭐⭐ _|
| 3️⃣ Je recommanderais cette formation.            ✅ Oui     |
|                                                              |
| ✅ Soumis le 15/03/2025 à 14:32 par Jean Dupont             |
+------------------------------------------------------------+
</pre>

---

## 💡 À retenir

- Les questionnaires sont **dynamiques** et adaptés au rôle de l’utilisateur.  
- Chaque utilisateur n’a accès **qu’à ses propres évaluations**.  
- Les retours sont **exportés automatiquement en PDF**.  
- Aucune modification n’est possible après soumission.  
- L’administrateur a un accès complet à l’ensemble des retours.

👉 **Prochaine section :** [Accès aux résultats (admin)](results.md)
