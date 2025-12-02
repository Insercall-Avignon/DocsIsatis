# 💬 Suivi de satisfaction

Le module de **suivi de satisfaction** permet de mesurer la qualité perçue des formations à travers les retours des **stagiaires**, **formateurs**, **employeurs** et **financeurs**.  
Ces évaluations sont essentielles pour assurer une **amélioration continue** des actions de formation.

---

## 🧭 Accès au module

- Disponible depuis le **tableau de bord administrateur** → **Évaluations → Suivi de satisfaction**
- Accessible selon le rôle :
  - **Administrateurs** → consultation et export des retours
  - **Stagiaires, formateurs, employeurs, financeurs** → remplissage du questionnaire dédié

Chaque questionnaire est lié à une **session** ou à une **inscription** précise.

---

## 🧾 Types de suivis disponibles

| Type de suivi              | Destinataire | Objectif principal                                       | Route associée       |
| -------------------------- | ------------ | -------------------------------------------------------- | -------------------- |
| **Satisfaction stagiaire** | Stagiaire    | Évaluer le contenu, le formateur et l’organisation       | `/feedback-trainee`  |
| **Retour formateur**       | Formateur    | Évaluer le déroulement de la session et la participation | `/feedback-former`   |
| **Satisfaction employeur** | Employeur    | Mesurer la pertinence de la formation pour le salarié    | `/feedback-employer` |
| **Satisfaction financeur** | Financeur    | Recueillir la perception de la qualité du dispositif     | `/feedback-financer` |

> 📅 L’envoi des liens de questionnaire se fait manuellement depuis l’espace administrateur.  
> Il n’existe pas encore d’envoi automatique “à froid”.

---

## 📋 Contenu des questionnaires

Chaque formulaire contient des questions adaptées au rôle du répondant.

**Exemples :**

### Stagiaire

- “Les objectifs annoncés ont-ils été atteints ?”
- “Le formateur était-il clair et disponible ?”
- “Recommanderiez-vous cette formation ?”

### Formateur

- “Le niveau du groupe était-il homogène ?”
- “Les moyens mis à disposition étaient-ils adaptés ?”

### Employeur / Financeur

- “La formation a-t-elle apporté un bénéfice mesurable ?”
- “Souhaitez-vous reconduire ce type d’action ?”

> Les formulaires sont rendus avec **Twig** et protégés par un **token de sécurité** (CSRF).

---

## 📈 Consultation et exploitation

Les résultats sont centralisés dans le tableau de bord administrateur :

- Affichage des **taux de réponse par type de questionnaire**
- Accès à chaque **grille d’évaluation individuelle**
- Possibilité d’**export PDF** via le template Twig
- Relance manuelle des participants n’ayant pas encore répondu

---

## 🧾 Exemple visuel

<pre>
+------------------------------------------------------------+
| Formation : Excel – Niveau 2 – Mars 2025                   |
|                                                            |
| ✅ 8/8 retours stagiaires reçus                            |
| ✅ 1/1 retour formateur reçu                               |
| 💶 1/1 retour financeur reçu                               |
|                                                            |
| Commentaires :                                             |
| - “Bonne pédagogie du formateur.”                          |
| - “Formation claire et rythmée.”                           |
|                                                            |
| 📤 [Exporter PDF]   🔁 [Relancer stagiaires]                |
+------------------------------------------------------------+
</pre>

---

## 💡 Bonnes pratiques

- Relancer les stagiaires ou formateurs qui n’ont pas encore répondu.
- Analyser les retours négatifs pour déclencher des **actions correctives**.
- Utiliser les PDF exportés pour les **dossiers Qualiopi** ou les **rapports qualité**.

---

## 🔒 Données et sécurité

- Les questionnaires sont **associés à un identifiant d’inscription** unique.
- Les résultats sont **non modifiables après soumission**.
- Les exports PDF sont générés via **Twig + mPDF**, avec un nom de fichier dynamique :
  `Grille_Evaluation-[Nom_Stagiaire]-[Date].pdf`
- Accès limité aux administrateurs et au personnel habilité.

---

## 🎯 Objectif du suivi

Le suivi de satisfaction permet à **Isatis Formation** de :

- garantir la **qualité et la cohérence des formations**,
- recueillir des **indicateurs mesurables** pour la démarche qualité,
- et valoriser l’expérience de chaque acteur du dispositif.

👉 **Prochaine section :** [Gestion des utilisateurs](../admin/users.md)
