# 📈 Accès aux résultats (Administrateur)

Les administrateurs disposent d’un espace dédié pour **consulter et exporter** les résultats des différents questionnaires d’évaluation.  
Ces informations permettent de suivre la qualité des formations, la progression des stagiaires et la satisfaction globale des intervenants.

---

## 🧭 Accès aux résultats

- Disponible depuis le **Tableau de bord administrateur** → **Évaluations → Résultats**
- Chaque **session de formation** possède sa propre fiche détaillée, incluant :
  - les retours **stagiaires**, **formateurs**, **employeurs** et **financeurs**,
  - les **évaluations de connaissances** (QCM, tests),
  - et les **documents PDF générés automatiquement**.

---

## 📊 Structure de la fiche de résultats

| Type d’évaluation             | Source / Route                        | Données visibles                       | Export disponible |
| ----------------------------- | ------------------------------------- | -------------------------------------- | ----------------- |
| 🧠 **Connaissances**          | `/inscription/{id}/feedback/trainee`  | Réponses QCM, score individuel         | 📤 PDF individuel |
| 🧍‍♂️ **Satisfaction stagiaire** | `/inscription/{id}/feedback/trainee`  | Questions à chaud, appréciations       | 📤 PDF            |
| 👨‍🏫 **Satisfaction formateur** | `/session/{id}/feedback/former`       | Retour sur déroulement et groupe       | 📤 PDF            |
| 🏢 **Satisfaction employeur** | `/inscription/{id}/feedback/employer` | Évaluation du bénéfice de la formation | 📤 PDF            |
| 💶 **Satisfaction financeur** | `/inscription/{id}/feedback/financer` | Retour administratif et global         | 📤 PDF            |

> 📄 Tous les résultats sont générés en **PDF via Twig**, avec un **footer et un template personnalisé** selon le rôle.

---

## ⚙️ Actions disponibles pour l’administrateur

- 🔍 **Consulter les résultats** directement depuis la fiche session ou inscription.
- 📤 **Exporter les retours** au format PDF (grille d’évaluation complète).
- 🔁 **Relancer un participant** si un questionnaire n’a pas encore été rempli.
- 🧩 **Comparer les retours** des différents acteurs d’une même session.

Les données sont **en lecture seule** : aucun résultat ne peut être modifié une fois soumis.

---

## 🧾 Exemple de fiche administrateur

<pre>
+------------------------------------------------------------+
| Formation : Excel – Niveau 2 – Mars 2025                   |
| Stagiaires inscrits : 8                                    |
|                                                            |
| ✅ 8/8 retours stagiaires reçus                            |
| ✅ 1/1 retour formateur reçu                               |
| ⚙️ 1/1 retour employeur reçu                               |
| 💶 1/1 retour financeur reçu                               |
|                                                            |
| Moyenne QCM initial : 13/20                                |
| Moyenne QCM final   : 17/20                                |
|                                                            |
| Commentaires :                                             |
| - “Formation claire et pratique.”                          |
| - “Bonne ambiance et rythme adapté.”                       |
|                                                            |
| 📤 [Exporter PDF]   🔁 [Relancer stagiaires]                |
+------------------------------------------------------------+
</pre>

---

## 🔒 Sécurité et confidentialité

- Les résultats sont **accessibles uniquement aux administrateurs**.
- Les réponses sont **verrouillées et non modifiables**.
- Tous les exports sont sécurisés par le **firewall Symfony** et utilisent un **template Twig PDF**.
- Les fichiers sont nommés dynamiquement selon le participant et la session  
  (ex. `Grille Evaluation - DUPONT Jean - 15-03-2025.pdf`).

---

## 💡 À retenir

- Les retours sont gérés **par rôle et par session** (stagiaire, formateur, employeur, financeur).
- Tous les formulaires et exports sont **centralisés dans le tableau de bord admin**.
- Les résultats permettent d’alimenter les **rapports qualité** et la **traçabilité des formations**.

👉 **Prochaine section :** [Suivi de satisfaction](feedback.md)
