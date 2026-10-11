[README.md](https://github.com/user-attachments/files/33310836/README.md)
# Atelier Reel — template modifiable

Le dossier contient `index.html` et `assets/ellipse.mp4`. Aucun outil de compilation n’est nécessaire. L’animation et la bande-son de la V.01 sont incluses ; ses retouches locales restent présentes.

## Modifier la composition

- Choisir un cadre dans la liste ou cliquer dessus.
- Le déplacer par sa poignée ; les flèches du clavier déplacent également la poignée (Maj pour aller plus vite).
- Modifier gauche, haut, largeur et hauteur, exprimés en pourcentage du reel.
- Choisir toujours visible, masqué, entre deux moments, ou apparition/disparition en boucle.
- La boucle par défaut du média A alterne tous les 16 temps à 117 BPM (8,205 s).
- Importer une image ou une vidéo pour remplacer l’emplacement provisoire. Les vidéos supplémentaires sont muettes ; la vidéo Ellipse contient la bande-son.
- Ajouter autant de cadres que nécessaire, jusqu’à 20. Chaque cadre a sa propre position et ses propres moments d’apparition.
- Les bordures sont placées dans une couche au-dessus de tous les contenus, pour rester fermées même quand les cadres se recouvrent.
- Le bandeau de transcription contient un texte libre à modifier ; cet outil ne produit pas automatiquement des sous-titres synchronisés.

« Enregistrer les réglages » sauvegarde dans ce navigateur seulement. Les grandes vidéos peuvent dépasser sa capacité : télécharger l’index ou exporter les réglages dans ce cas. Les médias importés sont intégrés au HTML/JSON exporté, ce qui peut produire un fichier volumineux. Rien n’est envoyé automatiquement sur un serveur.

« Télécharger index.html » produit le template avec les modifications. Conserver le dossier `assets` à côté pour l’ellipse d’origine. Remplacer l’ancien index sur GitHub pour publier les changements. Un navigateur contenant déjà des réglages locaux peut continuer à les afficher : utiliser « Revenir au modèle V.02 » pour charger les réglages du nouvel index.

## GitHub Pages

1. Créer ou ouvrir le dépôt souhaité sur GitHub.
2. Ajouter le **contenu** du dossier : `index.html`, `.nojekyll` et `assets/ellipse.mp4` à sa racine, avec le dossier assets intact.
3. Dans **Settings → Pages**, sélectionner **Deploy from a branch**, puis **main** et **/(root)**, et enregistrer.
4. GitHub affiche l’adresse du site après le déploiement.

Documentation : https://docs.github.com/en/pages/getting-started-with-github-pages/configuring-a-publishing-source-for-your-github-pages-site

Le site publié affiche la composition initiale et un éditeur. Les modifications de chaque visiteur restent locales jusqu’à export et remplacement de l’index dans le dépôt.

## Aperçu local

Ouvrir `index.html` dans un navigateur, ou depuis ce dossier lancer :

```sh
python3 -m http.server 8765
```

Puis ouvrir http://localhost:8765.

Ce template lit et compose les médias dans le navigateur. Il ne génère pas de MP4 ; les MP4 V.01 et V.02 livrés précédemment restent des fichiers séparés.
