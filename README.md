- URL site WEB :
- URL Notebook Observable :
- Nom :
- Prénom :
- Nom binome :
- Prénom binome :

# Remarques :

Décrire ici les éléments techniques remarquables de votre site (interactions, navigation, responsive, accessibilité...).
Idéalement avec des liens vers votre site et/ou [votre code](https://github.blog/news-insights/product-news/relative-links-in-markup-files/)

## Détail des éléments techniques

- **Accessibilité** : graphiques Plot avec `title`, `subtitle`, `caption` (→ `<figure>`/`<figcaption>`) et `ariaLabel` sur le `<svg>` ([index](src/pages/index.astro)) ; `lang="fr"` ; `<label>` associés à chaque `<select>` ; zone `aria-live` autour de la carte qui change ; popups et marqueurs Leaflet avec `title`/`alt`.
- **Leaflet** : [carte des établissements](src/pages/leaflet.astro) (2507 marqueurs, tuiles OpenStreetMap, cadrage automatique `fitBounds`).
- **GeoJSON + Plot côté client** : [carte des départements](src/pages/geojson.astro), choroplèthe (`Plot.geo`, projection conique conforme) redessinée à chaque changement des SELECT Période / Sexe / Âge ; les listes d'options sont construites côté serveur Astro.
- Les 4 DOM (Guadeloupe, Guyane, La Réunion, Martinique) sont dans les données de population mais absents du GeoJSON : ils n'apparaissent donc pas sur la carte.
