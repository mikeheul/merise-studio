# Historique des versions

Les versions les plus récentes sont en haut.

## 2.7.1

- **Licence et conditions d'utilisation élargies** : l'outil est gratuit pour
  l'apprentissage, l'enseignement et la conception courante de bases de
  données, y compris dans un cadre professionnel. La redistribution, la
  modification et la revente restent interdites sans accord de l'auteur.
- L'exemple du champ « Organisme » (visionneuse HTML) est désormais neutre.

## 2.7

- **Clé primaire modifiable depuis le MLD** : sur une table d'association
  (par exemple une association ternaire), un clic sur le badge **PK** d'une
  colonne permet de la retirer de la clé primaire tout en la gardant comme
  clé étrangère.
  - *Option A (recommandée)* : la cardinalité du lien passe à 1,1 dans le MCD ;
    le MLD, le MPD et le SQL suivent automatiquement.
  - *Option B* : modification dans le MLD uniquement, avec une pastille
    « clé retirée à la main » et un signalement dans la Qualité du modèle.
  - Garde-fou : une clé primaire garde toujours au moins une colonne.
- **Règle de passage Merise précisée** : dans une table d'association, seules
  les entités du côté « N » entrent dans la clé primaire ; une entité à
  cardinalité maximale 1 devient une clé étrangère hors clé.
  ⚠ Un projet existant contenant une association ternaire avec un lien (x,1)
  voit donc son MLD et son SQL évoluer.
- **Import SQL** : une table à clé composée avec une clé étrangère hors de la
  clé primaire est reconnue comme association ternaire (lien en 0,1 ou 1,1,
  signalé dans la liste des doutes).
- Aide mise à jour.

## 2.6

- **Fichier lié** : enregistrement dans un fichier précis au lieu de créer un
  nouveau JSON à chaque sauvegarde.
  - *Enregistrer* (Ctrl+S), *Enregistrer sous* (Ctrl+Maj+S), *Ouvrir* (Ctrl+O).
  - Sauvegarde automatique optionnelle, détection d'un conflit si le fichier a
    été modifié ailleurs, reprise du dernier fichier au démarrage.
  - Repli sur le téléchargement classique quand le navigateur ne gère pas
    l'API de fichiers.
  - Pastille d'état du fichier dans l'en-tête.
- En-tête réorganisé pour les fenêtres étroites (boutons réduits à des icônes).

## 2.5

- **Export du dossier de conception** en archive ZIP : schémas en images,
  scripts en texte, avec choix des éléments à exporter.
- **Import d'un script SQL** (rétro-ingénierie) : génération d'un MCD / MLD à
  partir d'un script existant, avec reconnaissance du SGBD, options
  d'heuristiques, liste des doutes et noms provisoires à confirmer.
- Aide : ajout de la sélection multiple avec Maj + sélection.

## 2.4 et antérieures

*Historique à compléter.*
