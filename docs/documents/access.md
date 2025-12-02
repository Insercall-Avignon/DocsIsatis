# 🔒 Accès et édition des documents

L’accès aux documents dans l’application **Isatis Formation** dépend du **rôle de l’utilisateur**, du **statut de la session** et de **l’état d’avancement de l’inscription**.  
Chaque document est protégé afin d’assurer la confidentialité et la traçabilité des actions.

---

## 👤 Accès selon le rôle

| Rôle utilisateur   | Peut consulter                       | Peut modifier                      | Peut supprimer | Peut télécharger |
| ------------------ | ------------------------------------ | ---------------------------------- | -------------- | ---------------- |
| **Stagiaire**      | ✅ Documents liés à ses inscriptions | ❌ Non                             | ❌ Non         | ✅ Oui           |
| **Formateur**      | ✅ Documents liés à ses sessions     | ✅ Supports, Feuilles d’émargement | ❌ Non         | ✅ Oui           |
| **Administrateur** | ✅ Tous les documents                | ✅ Tous les documents              | ✅ Oui         | ✅ Oui           |

> ℹ️ Tous les formulaires d’édition sont **protégés par un jeton CSRF** et nécessitent une **confirmation via modale** pour les actions critiques (suppression ou validation finale).

---

## ⏳ Accès selon le statut de l’inscription

Les documents deviennent disponibles **progressivement**, en fonction de l’avancement de la session :

| Statut de l’inscription      | Accès possible                                   |
| ---------------------------- | ------------------------------------------------ |
| **En attente de validation** | Aucun document disponible                        |
| **Acceptée**                 | Convocation, Convention, Documents préparatoires |
| **En cours**                 | Feuille d’émargement, Supports, QCM              |
| **Terminée**                 | Attestation, Questionnaire de satisfaction       |
| **Annulée**                  | Aucun accès (documents archivés)                 |

---

## 🧰 Actions disponibles

- 🔍 **Afficher** : ouverture du document dans une nouvelle fenêtre ou aperçu intégré.
- 🖋️ **Modifier** : édition des informations dynamiques (ex. changer le nom du formateur sur une convocation).
- 🗑️ **Supprimer** : disponible uniquement pour les administrateurs, avec confirmation modale.
- 💾 **Télécharger** : export en PDF généré automatiquement selon les données de la session.
- 🔄 **Mettre à jour** : pour certains documents dynamiques (feuille d’émargement, QCM), l’administrateur peut régénérer la dernière version.

---

## ⚙️ Sécurité et vérification

Chaque action de modification ou suppression déclenche :

- une **vérification des rôles** ;
- un **contrôle de propriété** (un formateur ne peut modifier que ses sessions) ;
- un **contrôle interne de sécurité Symfony**, garantissant que seules les actions autorisées sont exécutées (vérification des rôles, CSRF, droits d’accès).

Les documents sont générés via **Twig** (frontend) et protégés par le **firewall Symfony**, garantissant :

- aucune ressource publique sans authentification ;
- génération à la volée uniquement pour les utilisateurs autorisés.

---

## 📊 Exemple d’affichage

<pre>
+------------------------------------------------------------+
| Documents de la session : "Excel – Niveau 2 – Mars 2025"    \
|                                                              \
| 📄 Convocation.pdf             ✅ Téléchargeable             |
| 🧠 QCM_PreFormation.pdf        🔒 Visible uniquement admin   |
| 📝 Feuille_Emargement.pdf      🖋️ Modifiable (formateur)     |
| 📑 Attestation.pdf             ⏳ Disponible après session   |
+--------------------------------------------------------------+
</pre>

---

## 💡 Bon à savoir

- Les documents sensibles (factures, conventions) sont **visibles uniquement par les administrateurs et financeurs**.
- Toute tentative d’accès direct à un fichier via son URL est bloquée si l’utilisateur n’a pas les droits correspondants.
- Les documents sont **hébergés dans un répertoire sécurisé**, non exposé publiquement sur le serveur web.

👉 **Prochaine section :** [Types de questionnaires](../evaluations/types.md)
