# autodiag-landing

Landing page publique d'**AutoDiag Congo** (GitHub Pages).

Le dépôt source [`autodiag`](https://github.com/rograce2002/autodiag) est privé.
Cette vitrine publique envoie les clients ExpertDiag Shop et Mutuka vers
Google Play pour installer l'application.

## URL publique

https://rograce2002.github.io/autodiag-landing/

## Installation

Google Play est le moyen d'installation. Package : `com.autodiag.congo`.
Version affichée sur la page : **2.1.1**.

https://play.google.com/store/apps/details?id=com.autodiag.congo

## Activer GitHub Pages (une fois)

1. **Settings → Pages**
2. **Build and deployment → Source** : Deploy from a branch
3. **Branch** : `main` · **Folder** : `/ (root)`
4. Enregistrer — la page est en ligne sous 1 à 2 minutes

## Mettre à jour la version affichée

Quand une nouvelle version est publiée sur Google Play :

1. Mettre à jour la version dans `index.html` (texte visible, balises
   `description`, Open Graph et JSON-LD).
2. Vérifier que le badge pointe toujours vers
   `https://play.google.com/store/apps/details?id=com.autodiag.congo`.
3. Commit + push sur `main` — GitHub Pages republie la landing.

## Fichiers

| Fichier | Rôle |
|---|---|
| `index.html` | Page publique (GitHub Pages) |
| `assets/google-play-badge-fr.png` | Badge officiel Google Play (français) |
| `.nojekyll` | Désactive Jekyll sur Pages |
