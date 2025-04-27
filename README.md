# Projet de Bibliographie XML

## Présentation

Ce projet a été réalisé dans le cadre du cours **Document structuré et métadonnées** du Master 1 DEFI (Université Paris Nanterre).  
L'objectif était de concevoir une bibliographie structurée en XML, conforme à une DTD (Document Type Definition) définie manuellement.

Le projet comprend :
- `bibliographie.xml` : un fichier XML contenant la bibliographie.
- `bibliographie.dtd` : une DTD définissant la structure des données.

## Contenu

- **`bibliographie.xml`** : contient des notices de livres et d'articles scientifiques.
- **`bibliographie.dtd`** : définit les règles de structure et de validation pour le fichier XML.

## Structure du fichier XML

Le fichier est structuré autour d'une racine `<bibliographie>`, qui contient :
- Des éléments `<livre>`, chacun avec :
  - Attribut `isbn`
  - Balises enfants : `titre`, `auteur`, `pages`, `edition`, `collection`
- Des éléments `<article>`, chacun avec :
  - Attributs `issn` et `titreAbrege`
  - Balises enfants : `titre`, `auteur`, `periodique`, `datePublication`, `volume`, `numero`, `pagination`

### Extrait de la structure

```xml
<livre isbn="978-2-07-021-200-7">
  <titre>L'Étranger</titre>
  <auteur>Albert Camus</auteur>
  <pages>123</pages>
  <edition>
    <editeur>Gallimard</editeur>
    <annee>1942</annee>
  </edition>
  <collection>
    <titre>Collection Blanche</titre>
    <numero>1</numero>
  </collection>
</livre>
