# 📡 Projet SQL – Analyse du déploiement de la 4G Fixe en France (ARCEP 2024–2025)

Projet réalisé par Kitchi-Tawa Bourguinat en juillet-août 2025

---
Ce projet vise à analyser le déploiement des sites 4G fixe (4G Home) en France à partir des données publiques de l’ARCEP. Il s’appuie sur une [base de données publique](https://data.arcep.fr/mobile/4G_fixe/index.html) contenant plusieurs milliers de sites répartis sur le territoire, et propose une étude quantitative, géographique et temporelle de la couverture.

> 📅 Période d'analyse : T1 2024 à T1 2025

> 🗂 Données : arrêtés de l’ARCEP disponibles (open data)

> 🛠 Technologies : SQLite, SQL, Python (cartographie), LaTeX (rendu PDF)

---

## 🧭 Objectifs du projet

- Étudier la dynamique du déploiement 4G fixe dans les régions françaises
- Identifier les retards ou réussites régionales et départementales
- Cartographier les sites et la couverture
- Fournir une méthode d’analyse reproductible en SQL

---

## 📂 Structure du dépôt
├── latex # Rapport PDF final

├── cartographie/ # Scripts Python et cartes exportées (PNG)

## 🧰 Technologies utilisées

- **SQL (SQLite)** : traitement et analyse des données
- **Python** : génération de cartes (via `geopandas`, `matplotlib`)
- **LaTeX** : rédaction du rapport PDF
---

## 📊 Données utilisées

Les données utilisées proviennent du site officiel de l’[ARCEP](https://www.arcep.fr/), à travers les arrêtés trimestriels relatifs au New Deal Mobile. Les champs principaux incluent :

| Champ                  | Description                                              |
|------------------------|----------------------------------------------------------|
| `numero_site`          | Identifiant unique du site                               |
| `region`               | Nom de la région                                          |
| `departement`          | Département du site                                       |
| `sites_demandes`       | Site demandé dans un arrêté                               |
| `sites_mes`            | Site mis en service                                       |
| `x_lambert_93`, `y_lambert_93` | Coordonnées du barycentre en Lambert 93         |



## 📊 Analyses SQL réalisées

- Évolution trimestrielle des sites non encore mis en service
- Nombre de sites activés par région
- Taux de réalisation (activés / demandés)
- Comparaison départementale (Nouvelle-Aquitaine)
- Tableaux synthétiques et triés par performance
---

## 🗺️ Cartographie

Une cartographie simple a été réalisée pour localiser les sites demandés et ceux mis en service.

> Exemples :  
> ✅ Carte des sites activés  
> ⚠️ Carte des zones avec retards  
> 📍 Affichage par département (taux de réalisation)

---

## 📄 Rapport PDF

Le rapport complet (analyse + tableaux + cartes) est disponible 👉 [Lien vers le rapport](./rapport_SQL_4GFIXE_ARCEP.pdf) réalisé en LateX

---


## 📌 Idées d’amélioration

- Mise à jour automatique des données
---


[Carte-France](https://datawrapper.dwcdn.net/hgEC5/1/)
