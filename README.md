# Pullman Contact (GitHub Pages)

Ce dépôt sert une page unique qui affiche la fiche contact d'un employé (via un Google Apps Script) et génère un fichier vCard (.vcf) côté navigateur.

## Configuration requise
- Remplacez `DEPLOY_ID` dans `index.html` si besoin. Ici, il est déjà rempli avec :
```
AKfycbx6gzLF2I63qsrjP-NzAZSvJFpHk03HQEbHtM2mfe4cHovumTGAfSnwsTKGLw1Lt0stSA
```
- Sur vos cartes/QR, utilisez :  
`https://VOTRE_PSEUDO.github.io/pullman-contact/?id=CARTE01`

## Alimentation des données
Le Google Apps Script expose un endpoint JSONP :
`https://script.google.com/macros/s/AKfycbx6gzLF2I63qsrjP-NzAZSvJFpHk03HQEbHtM2mfe4cHovumTGAfSnwsTKGLw1Lt0stSA/exec?mode=jsonp&id=CARTE01&callback=onData`

Il renvoie `onData({ ... })` avec : `nom, prenom, poste, telephone, email, organisation, hotelName, hotelSite, logoDataUrl`.
