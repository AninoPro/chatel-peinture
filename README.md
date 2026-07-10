# Chatel Peinture — Site vitrine

Site one-pager pour **Chatel Peinture**, entreprise de peinture en bâtiment de
Raphaël Fouquet à Château-Renault (37).

Site statique (HTML/CSS/JS, sans dépendances), prêt à être déployé sur
**GitHub Pages**.

## Structure

```
.
├── index.html            # Page unique
├── css/styles.css        # Styles
├── js/main.js            # Menu mobile, révélations au scroll, lightbox
├── assets/
│   ├── favicon.svg
│   └── gallery/          # Photos de réalisations
├── .github/workflows/    # Déploiement automatique GitHub Pages
└── .nojekyll
```

## Aperçu en local

Ouvrir simplement `index.html` dans un navigateur, ou lancer un petit serveur :

```bash
python3 -m http.server 8000
# puis http://localhost:8000
```

## Déploiement sur GitHub Pages

1. Créer un dépôt GitHub et y pousser ce dossier (branche `main`).
2. Dans **Settings → Pages**, choisir **Source : GitHub Actions**.
3. À chaque `push` sur `main`, le workflow publie automatiquement le site.

## Nom de domaine (OVH — à faire plus tard)

1. Ajouter un fichier `CNAME` à la racine contenant le domaine, ex. :
   ```
   www.chatel-peinture.fr
   ```
2. Chez OVH (zone DNS), pour un domaine `chatel-peinture.fr` :
   - Un enregistrement **CNAME** `www` → `<utilisateur>.github.io.`
   - Pour le domaine racine, des enregistrements **A** vers les IP GitHub Pages :
     ```
     185.199.108.153
     185.199.109.153
     185.199.110.153
     185.199.111.153
     ```
3. Dans **Settings → Pages → Custom domain**, renseigner le domaine et cocher
   « Enforce HTTPS ».

## Contact / demande de devis

Aucune dépendance externe : le bouton « Écrire un email » est un lien `mailto:`
qui ouvre l'application de messagerie de l'utilisateur avec un message
pré-rempli (objet + trame de renseignements). L'adresse destinataire se change
directement dans le `href` du lien, dans `index.html` (section `#contact`).

## Informations entreprise

- **Raison sociale / nom commercial :** Chatel Peinture (Raphaël Fouquet)
- **Activité :** Travaux de peinture (NAF 43.34G)
- **SIRET :** 904 134 715 00013
- **Zone :** Château-Renault (37110) et environs (≈ 50 km)
- **Téléphone :** 06 58 15 56 56
- **Email :** raphaelfouquet@gmail.com
