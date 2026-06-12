# 🏀 Basketball Analytics

Application web de suivi physique et de statistiques de jeu pour le basketball — évolution des athlètes sur la saison.

## Fonctionnalités

- **Tableau de bord** — vue d'ensemble de tous les athlètes (moyennes par test) avec tri par colonne
- **Évolution** — courbes d'évolution par indicateur physique, profil de l'athlète (âge, taille, poids, poste, infos médicales), radar de notes /10 avec moyenne d'équipe en superposition, comparaison entre deux séances
- **Équipe** — évolution du score global de chaque athlète, classement, moyennes d'équipe
- **Matchs** — saisie des statistiques de jeu par joueur et par match (minutes, tirs à 2/3 pts, lancers francs, rebonds offensifs/défensifs, passes décisives, interceptions, contres, balles perdues), avec calcul automatique :
  - **Points** et **Eval** (efficacité — Pts + Reb + Passes + Interceptions + Contres − tirs à 2/3 pts ratés − balles perdues) par joueur et par match
  - Onglet **Évolution joueur** : courbe sur la saison + moyennes par match (points, Eval, rebonds, passes, interceptions, contres, balles perdues, minutes)
  - Onglet **Équipe** : totaux par match (points, Eval, rendement offensif = points / possessions) et ratios de rebonds offensif/défensif (si les stats de l'équipe adverse sont renseignées), plus les moyennes sur la saison
- **Gérer** — fiches athlètes (date de naissance, taille, poids, poste, informations médicales), export/import JSON pour sauvegarde

## Stockage des données

Toutes les données (athlètes, séances physiques, matchs) sont enregistrées dans le navigateur (`localStorage`). Pensez à utiliser **Exporter** régulièrement dans l'onglet "Gérer" pour sauvegarder vos données — un export crée un fichier `.json` que vous pouvez réimporter à tout moment.

## Utilisation

### Ouvrir localement

Double-cliquez sur `index.html` pour l'ouvrir dans votre navigateur. Aucune installation requise.

### Déployer sur GitHub Pages

1. Créez un nouveau dépôt GitHub (ex: `basketball-analytics`)
2. Uploadez `index.html` et `README.md`
3. Dans les **Settings** du dépôt → **Pages** → Source : `main` / `root`
4. L'application sera disponible à : `https://<votre-username>.github.io/basketball-analytics`

## Indicateurs physiques mesurés

| Indicateur | Description |
|---|---|
| CMJ | Counter Movement Jump — saut avec élan |
| SJ | Squat Jump — saut depuis position statique |
| Squat / PDC | Force relative au poids de corps |
| Test Australien | Force isométrique des ischio-jambiers (N) |
| T-Test | Test d'agilité (secondes) |
| VIFT | Vitesse maximale au 30-15 IFT (km/h) |
| VO2max | Consommation max d'oxygène (ml/kg/min) |

## Statistiques de match

| Indicateur | Formule |
|---|---|
| Points | 2pts marqués × 2 + 3pts marqués × 3 + lancers francs marqués |
| Eval | (Points + Rebonds + Passes + Interceptions + Contres) − (tirs à 2/3 pts ratés + balles perdues) |
| Possessions (équipe) | Tirs tentés + 0,44 × LF tentés + balles perdues |
| Rendement offensif (équipe) | Points équipe ÷ Possessions |
| Ratio rebond offensif (équipe) | Reb. off. équipe ÷ (Reb. off. équipe + Reb. def. adversaire) |
| Ratio rebond défensif (équipe) | Reb. def. équipe ÷ (Reb. def. équipe + Reb. off. adversaire) |

## Technologies

- HTML / CSS / JavaScript pur (aucune dépendance locale)
- [Chart.js](https://www.chartjs.org/) — graphiques
