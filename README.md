# Exodia

Application de suivi de budget : revenus, dépenses, frais fixes, crédits, épargne et patrimoine.
Elle fonctionne hors ligne une fois installée sur l'écran d'accueil de l'iPhone.

## Mettre en ligne avec GitHub Pages

1. Sur github.com, créez un dépôt **public** nommé `exodia` (bouton **+** puis **New repository**).
2. Dans le dépôt : **Add file** puis **Upload files**, et déposez tous les fichiers de ce dossier
   (`index.html`, `sw.js`, `manifest.webmanifest`, les icônes `icon-*.png` et ce `README.md`).
   Ils doivent être à la racine du dépôt, pas dans un sous-dossier. Validez avec **Commit changes**.
3. **Settings** puis **Pages** : dans *Branch*, choisissez `main` et `/ (root)`, puis **Save**.
4. Après une à deux minutes, l'adresse s'affiche : `https://VOTRE-NOM.github.io/exodia/`.

## Installer sur l'iPhone

1. Ouvrez l'adresse dans **Safari**, avec Internet.
2. **Partager** puis **Sur l'écran d'accueil**, puis **Ajouter**.
3. Ouvrez Exodia **depuis l'icône** (et non depuis Safari) au moins une fois avec Internet :
   l'application se met alors en mémoire et fonctionnera ensuite sans réseau.

## Récupérer ses données

Les données saisies dans la version Claude ne passent pas toutes seules dans la version GitHub.

1. Dans la version Claude : **⋯** puis **Copier mes données** (ou **Télécharger une sauvegarde**).
2. Dans l'application installée sur l'écran d'accueil : **Restaurer une sauvegarde**, collez, puis **Restaurer ces données**.

Les données sont enregistrées sur le téléphone, dans l'application de l'écran d'accueil.
Faites de temps en temps **Télécharger une sauvegarde** pour en garder une copie.

## Mettre à jour l'application

Remplacez `index.html` dans le dépôt, puis dans `sw.js` changez `exodia-v1` en `exodia-v2`
(puis v3, etc.). Rouvrez l'application avec Internet : la nouvelle version s'installe, vos données restent.
