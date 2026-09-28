# Référentiels de cotation DoctApp

Ce dépôt public contient **uniquement** le fichier `publication.json` : le référentiel de
cotation (NGAP / CCAM pour la médecine générale) téléchargé par l'application DoctApp au
démarrage, pour proposer au médecin les mises à jour des tarifs et des règles.

- **Aucune donnée de patient** ici, ni ailleurs dans ce dépôt.
- **Tarifs à vérifier** : chaque acte porte `aVerifier: true`. Rien n'est appliqué sans
  l'accord du médecin, qui compare et valide dans DoctApp ; les sources officielles
  (ameli.fr, CCAM) font foi.
- Le fichier est produit à partir du dépôt de l'application
  (`cargo run -p doctapp-core --example publier_referentiels > publication.json`), qui le
  valide avant publication. Ne pas le modifier à la main.

Adresse lue par l'application :
`https://raw.githubusercontent.com/Bo0x/doctapp-referentiels/main/publication.json`
