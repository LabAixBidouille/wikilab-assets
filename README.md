# wikilab-assets

Assets lourds (PDFs) du [Wiki@LAB](https://github.com/LabAixBidouille/wikilab),
externalisés pour alléger le repo principal et son artifact de déploiement
(cf. [wikilab#203](https://github.com/LabAixBidouille/wikilab/issues/203)).

## Servi sur

<https://assets.wikilab.labaixbidouille.com/> — GitHub Pages (déploiement
depuis la branche `main`, racine du repo).

Les fiches du wiki référencent ces fichiers via le composant `<PdfLink>`,
piloté par la variable d'environnement `ASSETS_BASE_URL` côté Docusaurus.
Exemple d'URL : `https://assets.wikilab.labaixbidouille.com/pdf/lets-steam/LS_R1AS01_LED_FR.pdf`.

## Organisation

```
pdf/<projet>/<fichier>.pdf
```

Un sous-dossier par projet (`lets-steam`, `mimesis`, `unplugged`,
`robots-meet-arts`, `steamcity`, `thedexterlab`, `youth-ai-lab`,
`magnetics`).

## Conventions

- Noms de fichiers **ASCII** uniquement : pas d'espace ni d'accent (sinon les
  URLs traînent des `%20`/`%C3%A9` fragiles). Convention `PROJET_Titre_FR.pdf`.
- `.nojekyll` à la racine : sert les fichiers bruts sans traitement Jekyll.

## Ajouter / mettre à jour un PDF

1. Déposer le fichier sous `pdf/<projet>/` avec un nom ASCII.
2. Commiter sur une branche, ouvrir une PR.
3. Référencer le fichier dans la fiche correspondante du repo `wikilab` via
   `<PdfLink href="/pdf/<projet>/<fichier>.pdf">Télécharger en PDF</PdfLink>`.
