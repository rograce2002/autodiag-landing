# autodiag-landing

Landing page publique de téléchargement **AutoDiag Congo** (GitHub Pages).

Le dépôt source [`autodiag`](https://github.com/rograce2002/autodiag) est privé ;
cette vitrine publique permet aux clients ExpertDiag Shop et Mutuka de
télécharger l'APK sans accès GitHub.

## URL publique

https://rograce2002.github.io/autodiag-landing/

## Activer GitHub Pages (une fois)

1. **Settings → Pages**
2. **Build and deployment → Source** : Deploy from a branch
3. **Branch** : `main` · **Folder** : `/ (root)`
4. Enregistrer — la page est en ligne sous 1 à 2 minutes

## Publier une nouvelle version APK

1. Copier l'APK release signé depuis le dépôt `autoDiag` :
   `app/build/outputs/apk/release/AutoDiag-Congo-vX.Y.Z-release.apk`
2. **Releases → Draft a new release** sur ce dépôt
3. Tag : `vX.Y.Z` (ex. `v2.0.0`)
4. Attacher l'APK avec le **même nom** que dans `index.html`
5. Mettre à jour le `href` du bouton dans `index.html` si la version change
6. Commit + push sur `main`

URL de téléchargement direct (format) :

```
https://github.com/rograce2002/autodiag-landing/releases/download/v2.0.0/AutoDiag-Congo-v2.0.0-release.apk
```

## Quand le Play Store sera validé

Mettre à jour `index.html` pour rediriger vers le Play Store, ou laisser
ExpertDiag Shop basculer `NEXT_PUBLIC_AUTODIAG_DOWNLOAD_URL` vers l'URL Play.

## Fichiers

| Fichier | Rôle |
|---|---|
| `index.html` | Page de téléchargement (GitHub Pages) |
| `.nojekyll` | Désactive Jekyll sur Pages |
