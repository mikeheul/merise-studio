# Merise Studio

Outil de modélisation de bases de données **hors ligne** pour l'enseignement :
MCD, MLD, MPD, UML, génération de scripts SQL et MongoDB.

> Version **2.7** · Windows (version portable, aucune installation)
> Usage pédagogique — voir [LICENCE.md](LICENCE.md)

![Icône de Merise Studio](icon.svg)

## Télécharger

Récupérez le fichier **`Merise Studio 2.7.0.exe`** dans la section
**Releases** de ce dépôt (ou à l'emplacement indiqué par votre enseignant).

> Le nom exact du fichier suit la version : `Merise Studio <version>.exe`.

## Démarrer

1. Placez le fichier `.exe` où vous voulez (Bureau, clé USB, dossier de cours).
2. Double-cliquez dessus : l'application démarre. **Rien n'est installé.**

### Avertissement Windows au premier lancement

L'application n'est pas signée numériquement. Windows peut afficher
*« Windows a protégé votre ordinateur »* :

1. cliquez sur **Informations complémentaires** ;
2. puis sur **Exécuter quand même**.

Sur un poste d'entreprise ou d'établissement, un antivirus ou une politique de
sécurité peut bloquer ce type de fichier : contactez alors votre
administrateur.

## Fonctionnalités

- **MCD** : entités, associations (y compris ternaires), cardinalités, héritage,
  identifiant relatif, notes et zones colorées.
- **MLD** : passage automatique MCD → MLD selon les règles de Merise, avec
  explication pas à pas ; **clé primaire modifiable** depuis le MLD.
- **MPD** et **scripts SQL** pour plusieurs SGBD (MySQL, PostgreSQL, SQL Server,
  Oracle, SQLite) ; export **MongoDB**.
- **UML** : diagrammes de classes.
- **Import d'un script SQL** : rétro-ingénierie vers un modèle MCD / MLD.
- **Qualité du modèle** : vérifications et conseils.
- **Export du dossier de conception** : archive ZIP (schémas en images,
  scripts en texte) avec choix des éléments.
- **Fichier lié** : enregistrement dans un fichier précis (Ctrl+S).
- Thèmes clair et sombre, recherche (Ctrl+K), aide intégrée.

## Vos données

- L'application fonctionne **entièrement sur votre poste** : aucune donnée
  n'est envoyée sur Internet, aucun compte, aucun traceur.
- Les projets sont enregistrés **localement** dans le profil Windows de
  l'utilisateur. Vider les données de l'application, ou utiliser un autre
  compte ou un poste réinitialisé à chaque session, fait perdre le travail non
  exporté.
- **Enregistrez régulièrement** vos projets en fichier (`Fichier →
  Enregistrer`, Ctrl+S) pour en garder une copie et pouvoir les ouvrir sur un
  autre poste.

## Questions fréquentes

**L'application ne se lance pas.**
Vérifiez que Windows ne bloque pas le fichier : clic droit sur le `.exe` →
*Propriétés* → cochez **Débloquer** si la case est présente.

**Je change de poste, comment retrouver mes projets ?**
Enregistrez vos projets en fichier et ouvrez-les sur l'autre poste
(`Fichier → Ouvrir`, Ctrl+O). Les projets mémorisés localement ne suivent pas
le fichier `.exe`.

**Puis-je en donner une copie à un camarade ?**
Non : la redistribution n'est pas autorisée sans accord de l'auteur. Indiquez
plutôt l'adresse de téléchargement. Voir [LICENCE.md](LICENCE.md).

## Licence

© 2026 Mickaël MURMANN. Tous droits réservés. Outil mis à disposition des
étudiants et enseignants du CESI pour un usage strictement pédagogique.
Détails dans [LICENCE.md](LICENCE.md).

L'application est fournie sans garantie : relisez et testez les scripts générés
avant tout usage en production.

## Contact

Mickaël MURMANN — CESI
