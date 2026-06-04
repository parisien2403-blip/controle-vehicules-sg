# Service Général — 4° RIISC

Application web (PWA) pour le **Service Général** : composition du poste, rondes parking et incendie, check-list SG, rapports PDF, import Excel/CSV du parc véhicules.

Fonctionne **hors ligne** sur téléphone après installation (cache local).

## Fichiers à publier (racine du dépôt)

| Fichier | Rôle |
|---------|------|
| `index.html` | Application |
| `insigne-embed.js` | Insigne PDF (obligatoire) |
| `sw.js` | Cache PWA |
| `manifest.json` / `manifest.webmanifest` | Installation écran d'accueil |
| `logo.png` | Icône de l’app sur l’écran d’accueil du téléphone |
| `phonix.png` | Insigne page de garde (dans l’app) |
| `_config.yml` | Config GitHub Pages |

## GitHub Pages

1. Créer un dépôt (ex. `controle-vehicules-sg`).
2. Pousser **tous** les fichiers ci-dessus à la racine de la branche `main`.
3. **Settings → Pages** → Source : **Deploy from branch** → `main` → dossier `/ (root)`.
4. Attendre 1 à 2 minutes, puis ouvrir :  
   `https://VOTRE_COMPTE.github.io/controle-vehicules-sg/`

> Si le dépôt s’appelle autrement, adaptez l’URL (`/nom-du-depot/`).

## Premier envoi avec Git (sur votre PC)

```bash
cd C:\Users\BOUQUET\Documents\controle-vehicules-sg
git init
git add index.html insigne-embed.js sw.js manifest.json manifest.webmanifest logo.png phonix.png _config.yml README.md LISEZMOI.txt
git commit -m "Publication PWA Service Général 4° RIISC"
git branch -M main
git remote add origin https://github.com/VOTRE_COMPTE/controle-vehicules-sg.git
git push -u origin main
```

(Remplacez `VOTRE_COMPTE` et le nom du dépôt.)

## Test en local

Double-clic sur `LANCER.bat` ou ouvrir `index.html` via un petit serveur local.

## Mise à jour de l’app sur le téléphone

Après un `git push`, sur le téléphone : rouvrir l’URL GitHub Pages (ou vider le cache / réinstaller la PWA) pour prendre la nouvelle version du service worker (`sw.js`).
