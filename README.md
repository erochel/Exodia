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

## Saisir une dépense à chaque paiement (Apple Pay)

Un raccourci iPhone copie le montant et le commerçant à chaque paiement Apple Pay ;
Exodia les reprend avec le bouton **Ajouter le dernier paiement** (onglets Mois et Dépenses).

1. App **Raccourcis** → onglet **Automatisation** → **+** → **Transaction**.
2. Choisissez vos cartes, laissez toutes les catégories, cochez **Exécuter immédiatement** → **Suivant** → **Nouvelle automatisation vide**.
3. Ajoutez l'action **Texte** et écrivez : `EXODIA;` puis la variable **Montant**, `;`, la variable **Commerçant**, `;`, la variable **Date actuelle**.
   Exemple de résultat : `EXODIA;12,50 €;Carrefour;15/11/2026 23:20`
4. Ajoutez l'action **Copier dans le presse-papiers**.
5. Ajoutez l'action **Afficher une notification** : « Paiement prêt pour Exodia ».
6. Après un paiement, ouvrez Exodia, touchez **Ajouter le dernier paiement**, puis **Coller** quand l'iPhone le demande.
   Montant, libellé et catégorie sont remplis : vérifiez et touchez **Enregistrer**.

Ne fonctionne qu'avec les paiements Apple Pay (iPhone ou montre), pas avec la carte physique.
L'adresse `https://erochel.github.io/exodia/?montant=12,50&commercant=Carrefour` ouvre aussi le formulaire prérempli,
mais dans Safari, dont les données sont séparées de l'application de l'écran d'accueil.

## Budgets et catégories

- Onglet **Dépenses** → **Fixer un budget**, ou touchez une catégorie. Exodia prévient à 80 %, et plus tôt si le rythme de dépenses mène à un dépassement.
- La catégorie est choisie automatiquement d'après le libellé (vos habitudes, puis les enseignes connues : Carrefour → Alimentaire, Total → Essence…).

## Mettre à jour l'application

Remplacez `index.html` dans le dépôt, puis dans `sw.js` augmentez le numéro de `CACHE`
(exodia-v5 → exodia-v6, etc.). Rouvrez l'application avec Internet : la nouvelle version s'installe, vos données restent.
