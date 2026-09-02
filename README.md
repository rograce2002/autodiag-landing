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
2. Uploader sur Firebase Storage (bucket hub DiagSync) :

```bash
gsutil -h "Content-Type:application/vnd.android.package-archive" \
  cp AutoDiag-Congo-vX.Y.Z-release.apk \
  gs://studio-1332800635-78fb6.firebasestorage.app/public/autodiag/releases/AutoDiag-Congo-vX.Y.Z-release.apk
```

3. Mettre à jour le `href` du bouton dans `index.html` (URL Firebase Storage)
4. Mettre à jour `NEXT_PUBLIC_AUTODIAG_PUBLIC_APK_URL` dans ExpertDiag Shop
5. Commit + push sur `main` (landing) ; redéployer App Hosting si besoin

URL de téléchargement direct (format Firebase Storage) :

```
https://firebasestorage.googleapis.com/v0/b/studio-1332800635-78fb6.firebasestorage.app/o/public%2Fautodiag%2Freleases%2FAutoDiag-Congo-v2.0.0-release.apk?alt=media
```

Fallback GitHub Release (optionnel) :

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
