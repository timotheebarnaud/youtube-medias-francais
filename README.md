# YouTube : comment se comportent les audiences des médias français ?

*Analyse comparative des performances YouTube de 20 médias français à partir de l'API YouTube Data v3*

## Visualisations

- [Cadence de publication vs performance médiane (scatter plot – Datawrapper)](https://www.datawrapper.de/_/qf8oY/?v=3)
- [Mobilisation des bases d'abonnés (bar chart – Flourish)](https://public.flourish.studio/story/3505255/)
- [Stabilité des audiences par média (bar chart – Datawrapper)](https://www.datawrapper.de/_/6BXXQ/)

## Méthodologie

Les données proviennent de l'API **YouTube Data v3**. Pour chaque média, les **50 dernières vidéos longues** (≥ 3:01) ont été analysées, excluant ainsi les YouTube Shorts. Les indicateurs calculés : vues médianes, ratio vues/abonnés, cadence de publication sur 30 jours, et variabilité des performances. La **médiane** est privilégiée à la moyenne pour limiter l'impact des vidéos virales, et les comparaisons reposent sur des **indicateurs relatifs** plutôt que des volumes bruts.

Les performances des médias ont été analysées sur la période du **13/11/2025 au 13/12/2025**.

**Limites** : 

L'analyse porte sur une période plutôt courte et ne décrit pas des tendances de long terme. Les performances peuvent être influencées par l'actualité.
La suppression des vidéos de moins de 3 minutes est un choix éditorial assumé, mais qui peut écarter les stratégies de certains médias sur les YouTube Shorts.

## Organisation du dépôt

```
├── data/
│   ├── raw/            # Données brutes (liste des médias)
│   └── clean/          # Dataset final avec indicateurs
├── notebooks/
│   └── analyse_youtube_medias.ipynb
├── visualisations/
└── README.md
```

## Outils

Python (pandas, requests) · API YouTube Data v3 · Jupyter Notebook · Datawrapper · Flourish

---

Projet réalisé par **Timothée Barnaud**.