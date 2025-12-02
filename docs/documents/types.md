# 📂 Types de documents

L’application de gestion de formations Isatis Formation intègre un système complet de **documents générés automatiquement par le système**, selon le type de session et le rôle de l’utilisateur.

Chaque document est **lié à une inscription** et devient **visible ou modifiable** selon l’état d’avancement de la session.

---

## 🗂️ Catégories principales

### 1. Documents administratifs

- **Convocation** : document envoyé au stagiaire après validation de l’inscription, contenant les informations de la session (dates, lieu, formateur, horaires, etc.).
- **Feuille d’émargement** : liste de présence permettant aux stagiaires et formateurs de signer durant la formation.
- **Attestation de présence** : générée automatiquement à la fin de la session, une fois les présences validées.

### 2. Documents pédagogiques

- **Programme de formation** : décrit le contenu, les objectifs et les compétences visées.
- **Supports de cours** : fichiers PDF ou ressources partagées par le formateur pendant la formation.
- **QCM / Questionnaire de connaissances** : à compléter en ligne avant, pendant ou après la session selon le type d’évaluation.

### 3. Documents financiers

- **Devis / Convention de formation** : documents établis entre l’organisme et le financeur avant le début de la formation.
- **Facture** : émise à la fin de la session, disponible uniquement pour les administrateurs et financeurs.
- **Feuille de remboursement / justificatif** : selon le cas de prise en charge.

### 4. Documents d’évaluation

- **Questionnaire de satisfaction (stagiaire)** : envoyé après la formation.
- **Questionnaire d’évaluation formateur** : destiné aux formateurs pour évaluer la session.
- **Synthèse des résultats** : réservée aux administrateurs, permettant de visualiser les retours consolidés.

---

## 🔒 Gestion de la visibilité

| Rôle utilisateur   | Lecture                              | Modification                    | Téléchargement |
| ------------------ | ------------------------------------ | ------------------------------- | -------------- |
| **Stagiaire**      | ✅ Oui (documents liés à sa session) | ❌ Non                          | ✅ Oui         |
| **Formateur**      | ✅ Oui (documents de ses sessions)   | ✅ Oui (documents pédagogiques) | ✅ Oui         |
| **Administrateur** | ✅ Oui (tous documents)              | ✅ Oui                          | ✅ Oui         |

---

## 🧩 Dépendance au statut de l’inscription

Certains documents apparaissent uniquement à **certaines étapes** :

| Étape de l’inscription   | Documents disponibles                                |
| ------------------------ | ---------------------------------------------------- |
| **Avant la formation**   | Convocation, Convention, Questionnaire initial       |
| **Pendant la formation** | Feuille d’émargement, Supports, QCM                  |
| **Après la formation**   | Attestation, Questionnaire de satisfaction, Synthèse |

---

## 📊 Exemple visuel

<pre>
+------------------------------------------------------------+
| Documents liés à : Excel – Niveau 2 – Mars 2025             \
|                                                              \
| 📄 Convocation.pdf                ✅ Téléchargeable          |
| 🧾 Convention_Formation.pdf       🔒 Accès admin uniquement  |
| 🧠 QCM_PreFormation.pdf           🕒 Disponible à J-2        |
| 📝 Questionnaire_Satisfaction.pdf ⏳ Disponible après session|
+--------------------------------------------------------------+
</pre>

👉 **Prochaine section :** [Accès et édition](access.md)
