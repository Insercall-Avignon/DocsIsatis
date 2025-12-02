# 🗓️ Gestion des sessions de formation

Le module **Administration → Sessions** permet aux administrateurs de **créer, modifier et suivre** les sessions de formation proposées par Isatis Formation.  
C’est le cœur du pilotage de l’activité de formation.

---

## 🧭 Accès

- Menu principal : **Administration → Sessions**  
- Réservé aux utilisateurs disposant du rôle `ROLE_ADMIN`.  
- Vue principale sous forme de **cartes de sessions** listant les informations essentielles.

---

## 📋 Fonctions principales

| Fonction | Description |
|-----------|--------------|
| ➕ **Créer une session** | Accès au formulaire complet de création (titre, dates, formateur, lieu, etc.). |
| ✏️ **Modifier une session** | Mise à jour des informations principales ou des participants. |
| ❌ **Supprimer une session** | Supprime définitivement la session après confirmation. |
| 📄 **Accès rapide** | Lien direct vers les inscriptions, documents et évaluations liées. |
| 🔍 **Recherche / tri / pagination** | Système de filtrage performant pour naviguer dans la liste des sessions. |

---

## 🧾 Détails d’une session

Chaque session affiche ses informations principales :

| Champ | Description |
|--------|--------------|
| **Titre** | Nom de la formation (ex : Excel – Niveau 2) |
| **Dates** | Période de la session (ex : du 10 au 12 mars 2025) |
| **Formateur** | Utilisateur désigné comme intervenant principal |
| **Lieu** | En présentiel ou à distance |
| **Capacité** | Nombre maximum de participants |
| **Statut** | Brouillon, Ouverte, Clôturée |

<pre>
+------------------------------------------------------------+
| Formation : Excel – Niveau 2                               |
| Dates : 10 → 12 mars 2025                                  |
| Formateur : Marie Dupuis                                   |
| Lieu : Lyon (présentiel)                                   |
| Statut : ✅ Ouverte                                         |
| Participants : 8/10                                         |
|                                                            |
| [👥 Inscriptions] [📄 Documents] [📈 Évaluations] [✏️ Edit] |
+------------------------------------------------------------+
</pre>

---

## 🧩 Gestion des participants

L’administrateur peut :

- **Inviter des stagiaires** à rejoindre une session via leur adresse e-mail.  
- **Valider ou refuser** les demandes d’inscription reçues.  
- **Associer un formateur** à la session.  
- Suivre le **statut d’inscription** de chaque stagiaire :
  - En attente
  - Acceptée
  - Refusée
  - Terminée

> Chaque invitation envoie un email automatique contenant un lien sécurisé vers le formulaire de participation.

---

## 📎 Documents liés à la session

Les sessions sont connectées à plusieurs types de documents :

- Convocation
- Feuille d’émargement
- Attestation de présence
- QCM / Évaluations formatives

Ces documents deviennent accessibles automatiquement selon **l’état de la session** (ex : attestation uniquement après la clôture).

---

## 📊 Suivi des inscriptions

Depuis l’onglet *Inscriptions*, l’administrateur visualise :

| Donnée | Description |
|--------|--------------|
| Nom du stagiaire | Lié à sa fiche utilisateur |
| Statut | En attente / Acceptée / Refusée |
| Date d’inscription | Générée automatiquement |
| Actions rapides | Voir profil, modifier statut, supprimer |

---

## ⚙️ Bonnes pratiques

- **Clôturer** les sessions dès la fin de la formation pour activer les évaluations et documents post-formation.  
- Vérifier que tous les **stagiaires invités** ont bien validé leur participation avant le démarrage.  
- Utiliser le **tri par statut** pour suivre les sessions à venir, en cours ou terminées.

---

## 🔒 Sécurité

- Chaque modification ou suppression déclenche une **modale de confirmation**.  
- Les formulaires sont protégés par des **tokens CSRF**.  
- Les actions sont **journalisées** (historique d’activité disponible pour audit).

---

## 💡 Astuce

> Pour les sessions récurrentes, il est possible de **dupliquer** une session existante pour gagner du temps lors de la création.

---

👉 **Prochaine section :** [Gestion des documents](documents.md)
