# Historique des versions

Les versions les plus récentes sont en haut.

## 2.8

- Correctif Electron : les confirmations (nouveau projet, exemple, import) sont désormais intégrées à l'application ; les boîtes natives pouvaient bloquer la saisie au clavier (renommage d'entité impossible).
- Sections repliables de la barre latérale en cartes (bordure au survol, espacement confortable, ligne « Tout replier / Tout déplier » alignée).

- **Barre latérale en sections repliables** : Attributs, Liens, Héritage et
  Vérifications se replient d'un clic (repliées par défaut). Le titre résume le
  contenu quand la section est fermée, l'état est mémorisé, et deux liens
  permettent de tout replier ou tout déplier.
- **Contrainte d'héritage mise en évidence** : le badge X, T ou XT est visible
  sur le titre de la section Héritage même repliée, et le choix actif est
  surligné. Un sous-type affiche la contrainte de sa mère, avec un lien pour
  la modifier.
- **Points d'attache des liens d'héritage** : comme pour les liens classiques, sélectionnez un héritage et glissez les poignées rondes pour déplacer les extrémités de la flèche sur l'entité fille ou mère (double-clic sur une poignée ou bouton « Remettre en automatique » pour revenir au placement automatique).
- **Correctif** : des champs de renommage (nom d'entité en cours d'édition) pouvaient rester affichés après la création d'entités ou l'ouverture d'un autre projet ; ils sont désormais toujours fermés.
- Nouvel exemple **Contraintes d'héritage (X, T, XT)** dans Fichier > Exemples.

- **Contraintes d'héritage** : sur une entité mère, choisissez une contrainte
  portant sur ses sous-types : **X** (exclusion : au plus un sous-type),
  **T** (totalité : au moins un) ou **XT** (partition : exactement un).
  - Une pastille s'affiche près des triangles d'héritage du MCD. Un petit
    « + » apparaît au survol quand aucune contrainte n'est définie ; un
    double-clic sur la pastille fait défiler X, T, XT, aucune.
  - La contrainte est aussi réglable dans la section « Héritage » de l'entité
    mère, avec une explication pour chaque choix.
  - Elle est **documentée** dans l'explication du MLD, en commentaires du
    script SQL, sur le diagramme UML (`{disjoint}`, `{complete}`,
    `{disjoint, complete}`) et dans la Qualité du modèle (contrainte avec un
    seul sous-type ou sans sous-type, héritage sans contrainte).
  - Elle n'est **pas appliquée** par le schéma SQL : elle est à contrôler dans
    l'application ou par un déclencheur.
  - Les projets existants s'ouvrent sans contrainte, rien ne change pour eux.

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
