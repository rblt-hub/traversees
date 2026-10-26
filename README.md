# Traversées — mise en ligne sur GitHub Pages

Site statique prêt à publier : index.html et cinq images dans images/. Aucun outil de compilation nécessaire.

## 1. Créer un dépôt séparé

Sur le même compte GitHub que ton site d’artiste, crée un dépôt public nommé `traversees`. Ne remplace pas le dépôt de rubenbrulat.com.

Avec GitHub Desktop sur Mac : clone ce nouveau dépôt, ouvre son dossier dans le Finder, puis copie le CONTENU de cette archive à la racine. Le fichier index.html doit être directement dans le dépôt, pas dans un sous-dossier. Conserve le dossier images avec son nom exact.

Dans GitHub Desktop : inscris un résumé (« Mise en ligne de Traversées »), clique Commit to main, puis Push origin (ou Publish repository si le dépôt est encore local ; décoche alors Keep this code private).

Tu peux aussi utiliser Add file > Upload files sur GitHub pour téléverser index.html et le dossier images, puis enregistrer le commit.

## 2. Activer Pages

Dans le dépôt : Settings > Pages > Build and deployment.
Choisis Deploy from a branch, puis main et / (root), puis Save.
Attends le déploiement, puis utilise Visit site dans Settings > Pages pour ouvrir l’adresse effective. Le délai peut atteindre 10 minutes.

Le site peut d’abord être consulté à l’adresse fournie par GitHub. Si ton domaine d’artiste est configuré au niveau du site utilisateur, l’adresse du projet peut hériter de ce domaine. Utilise donc l’adresse affichée par Pages plutôt que d’en deviner une.

## 3. Raccorder traversees.earth

Le nom de domaine prévu pour ce projet est traversees.earth. Ne modifie pas les réglages de rubenbrulat.com.

Quand le site fonctionne sur Pages :
1. Dans Settings > Pages > Custom domain, saisis traversees.earth et enregistre.
2. GitHub ajoute un fichier CNAME au dépôt. Dans GitHub Desktop, fais Fetch origin puis Pull origin pour récupérer ce fichier localement et le conserver lors des prochains changements.
3. Chez le gestionnaire DNS de traversees.earth, remplace uniquement les entrées web de ce domaine qui pointent vers l’ancien hébergeur par les réglages ci-dessous. Conserve les enregistrements liés aux emails et aux vérifications de domaine.

Type | Nom | Valeur
--- | --- | ---
A | @ | 185.199.108.153
A | @ | 185.199.109.153
A | @ | 185.199.110.153
A | @ | 185.199.111.153
CNAME | www | TON-IDENTIFIANT-GITHUB.github.io

Remplace TON-IDENTIFIANT-GITHUB par ton identifiant réel, sans ajouter /traversees. Supprime les anciennes entrées A, AAAA ou CNAME concurrentes pour @ et www si elles pointent vers l’ancien hébergeur. Les changements DNS peuvent prendre jusqu’à 24 heures.

Une fois le domaine validé, active Enforce HTTPS dans Settings > Pages ; sa disponibilité peut aussi prendre jusqu’à 24 heures.

Aucun fichier CNAME n’est prérempli dans cette archive : GitHub le créera quand tu choisiras ton domaine. Cela permet de tester le site avant de basculer traversees.earth.

## 4. Vérifier puis mettre à jour

Vérifie les cinq photos, la disposition mobile, les liens « partir ↗ » vers rubenbrulat@gmail.com et le lien artistique.
Pour chaque mise à jour : remplace les fichiers dans le dossier local du dépôt, Commit to main puis Push origin. Copier dans le dossier du Mac ne suffit pas à publier.

Documentation officielle :
https://docs.github.com/en/pages/getting-started-with-github-pages/creating-a-github-pages-site
https://docs.github.com/en/pages/configuring-a-custom-domain-for-your-github-pages-site/managing-a-custom-domain-for-your-github-pages-site
