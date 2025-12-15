# YouTube : comment se comportent les audiences des médias français ?

*Analyse comparative des performances YouTube de médias français à partir de l’API YouTube Data v3*

---

## Résumé du projet

Ce projet analyse la performance des chaînes YouTube de médias français à partir de données
récupérées via l’API YouTube Data v3.  
L’objectif est de comparer leurs stratégies de publication, l’engagement relatif de leurs
audiences et la régularité de leurs performances, à partir d’indicateurs simples,
comparables et défendables éditorialement.

Visualisations interactives disponibles en ligne :
- https://www.datawrapper.de/_/qf8oY/?v=3
- https://public.flourish.studio/story/3505255/
- https://www.datawrapper.de/_/6BXXQ/

---

## Pourquoi ce projet

Ce projet a été conçu comme un exercice de datajournalisme appliqué, avec l’objectif de
produire une analyse comparative rigoureuse, compréhensible pour un lecteur non technique.

Il s’inscrit dans une logique proche des travaux menés par la Cellule Data & Lab de *mind*.

---

## Questions journalistiques

Le projet cherche à répondre à trois questions principales :

1. Les médias privilégient-ils le volume de publication ou l’impact par vidéo sur YouTube ?
2. Les bases d’abonnés se mobilisent-elles de la même façon selon les médias ?
3. Les performances des vidéos sont-elles stables ou variables d’un média à l’autre ?

---

## Sources de données

Les données utilisées proviennent exclusivement de l’API **YouTube Data v3**, notamment :

- Statistiques des vidéos (vues, durée, date de publication)
- Informations de chaîne (nombre d’abonnés)

Les données ont été collectées sur une période récente, identique pour l’ensemble des médias
analysés.

---

## Méthodologie

### Sélection des vidéos

Seules les **vidéos longues** ont été retenues (durée ≥ 181 secondes), afin d’exclure de
manière robuste les formats courts (YouTube Shorts), qui viendraient fausser la comparabilité entre médias.

Pour chaque chaîne, l’analyse repose sur les **50 dernières vidéos longues publiées**.
La sélection s’effectue après :
- pagination complète des résultats via l’API,
- filtrage par durée,
- conservation des 50 premières vidéos valides.

Ce choix vise à comparer des volumes équivalents de contenus entre médias.

---

### Indicateurs calculés

Les indicateurs suivants ont été calculés pour chaque média :

- **Vues médianes par vidéo**
- **Ratio vues / abonnés**
- **Vues pour 1 000 abonnés**
- **Cadence de publication sur 30 jours**
- **Variabilité des performances** (écart-type des vues)
- **Variabilité relative** (écart-type rapporté à la médiane)

---

### Choix méthodologiques clés

- La **médiane** est privilégiée à la moyenne afin de limiter l’impact des vidéos virales.
- Les comparaisons reposent sur des **indicateurs relatifs**, plutôt que sur des volumes bruts.
- L’objectif est de comparer des **comportements et des stratégies**, pas de produire des
classements absolus ou normatifs.

Le pipeline de collecte et de calcul a été conçu pour être **réutilisable** sur d’autres
chaînes ou sur des périodes différentes.

---

## Visualisations produites

Les indicateurs calculés ont servi de base à trois visualisations principales :

1. **Sur YouTube, publier davantage ne garantit pas de meilleures audiences**
   Comparaison de 20 médias français selon leur cadence de publication et la performance médiane de leurs vidéos longues
   *(scatter plot – Datawrapper)*

   Voir la visualisation : https://www.datawrapper.de/_/qf8oY/?v=3

2. **Les bases d’abonnés des médias français ne se mobilisent pas de la même façon sur YouTube**
   Vues médianes des 50 dernières vidéos longues, pour 1 000 abonnés 
   *(bar chart horizontal – Flourish)*

   Voir la visualisation : https://public.flourish.studio/story/3505255/
   
3. **Stabilité ou fortes variations : comment se comportent les audiences des médias sur YouTube**  
   Variabilité relative des vues des vidéos longues de 20 médias français  autour de la performance médiane
   *(bar chart horizontal – Datawrapper)*

   Voir la visualisation : https://www.datawrapper.de/_/6BXXQ/

Ces visualisations constituent le cœur éditorial du projet.

---

## Limites et précautions d’interprétation

- La suppression des vidéos de moins de 3 minutes est un choix éditorial assumé, 
mais qui peut écarter les stratégies de certains médias sur les YouTube Shorts.
- Les performances peuvent être influencées par l’actualité et le contexte éditorial.
- L’analyse porte sur une période récente et ne prétend pas décrire des tendances de long terme.

Les résultats doivent donc être interprétés comme des **indicateurs comparatifs**, et non
comme des mesures absolues de performance ou de qualité éditoriale.

---

## Organisation du dépôt
```
├── data/
│  
├── data/
│ ├── raw/ # données brutes issues de l’API
│ └── clean/ # dataset final utilisé pour les visualisations
├── notebooks/
│ └── analyse_youtube_medias.ipynb
├── visualizations/
│ ├── graphique_1.png
│ ├── graphique_2.png
│ └── graphique_3.png
└── README.md
```

---

## Outils utilisés

- Python (pandas, requests)
- API YouTube Data v3
- Jupyter Notebook
- Datawrapper
- Flourish

---

## À propos

Projet réalisé par **Timothée Barnaud** dans le cadre d’une candidature au poste de
datajournaliste au sein de la **Cellule Data & Lab de *mind***.