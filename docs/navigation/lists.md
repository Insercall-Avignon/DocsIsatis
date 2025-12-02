# Affichage et recherche de données

## 📋 Présentation générale

L’application **Isatis Formation** propose des **listes interactives** pour visualiser et gérer les informations selon le rôle de l’utilisateur.

Les données sont présentées :

- Sous forme de **cartes** regroupant les informations principales
- Ou sous forme de **tableaux** pour les vues administratives

> 💡 L’affichage varie selon le rôle : stagiaire, formateur ou administrateur.

---

## 🧩 Structure des cartes

Chaque carte affiche les informations principales d’un élément (session, utilisateur, inscription…).

### Contenu typique :

- Titre (ex : _Nom de la formation_)
- Informations clés (dates, lieu, statut, formateur, nombre d’inscrits)
- Boutons d’action (voir, modifier, supprimer, accéder aux documents)
- Icônes de raccourcis contextuels 🔗

---

## 🔍 Recherche

Le moteur de recherche permet de filtrer instantanément les données affichées.

### Fonctionnalités :

- Recherche **en temps réel**
- Filtrage sur plusieurs champs (nom, date, email, statut…)
- Compatible avec le tri et la pagination
- Affiche “Aucun résultat trouvé” si nécessaire

### Exemples :

- Rechercher un utilisateur par nom ou email
- Rechercher une session par intitulé ou formateur
- Rechercher une inscription par date ou statut

---

## ↕️ Tri

Permet d’ordonner les résultats **ascendant / descendant** selon :

- Nom / Intitulé
- Date
- Statut
- Rôle (pour les utilisateurs)

> S’applique automatiquement à la liste actuelle.

---

## 📄 Pagination

Divise les longues listes en **pages** pour éviter la surcharge du navigateur.

### Fonctionnalités :

- Navigation simple (numéros ou flèches)
- Nombre d’éléments par page configurable
- Compatible avec recherche et tri
- Sauvegarde du **dernier état** pour chaque utilisateur

---

## ⚙️ Actions rapides

Chaque carte ou ligne peut inclure :

- 📝 Modifier
- 🔍 Voir le détail
- ❌ Supprimer (avec confirmation)
- 📄 Accéder aux documents
- ➕ Ajouter une inscription

> Ces actions dépendent du rôle et des permissions.

---

## 🔐 Sécurité et confirmation

- Toutes les actions sensibles déclenchent une **modale de confirmation**.
- Les requêtes sont protégées par un **jeton CSRF**.
- Les filtres et recherches sont validés côté serveur.

---

## 💡 Astuces

- Combinez recherche + tri pour gagner du temps.
- Utilisez les filtres par rôle ou statut pour isoler rapidement un groupe.
- Les cartes évoluent dynamiquement selon l’état des inscriptions et documents.

---

## ➡️ Pour aller plus loin

👉 **Prochaine section :** [Paramètres et notifications](settings.md)
