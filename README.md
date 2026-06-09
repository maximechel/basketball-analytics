# 🏀 Basketball Analytics

Application web d'analyse physique pour le basketball — visualisation des indicateurs de performance athlétique.

## Fonctionnalités

- **Tableau de bord** — vue d'ensemble de tous les athlètes avec tri par colonne
- **Fiche athlète** — graphique radar des notes /10, détail des indicateurs (CMJ, SJ, VO2max, etc.)
- **Comparaison** — graphiques comparatifs entre athlètes sur chaque indicateur
- **Import Excel** — mise à jour des données via glisser-déposer d'un nouveau fichier `.xlsx`

## Utilisation

### Ouvrir localement

Double-cliquez sur `index.html` pour l'ouvrir dans votre navigateur. Aucune installation requise.

### Déployer sur GitHub Pages

1. Créez un nouveau dépôt GitHub (ex: `basketball-analytics`)
2. Uploadez `index.html` et `README.md`
3. Dans les **Settings** du dépôt → **Pages** → Source : `main` / `root`
4. L'application sera disponible à : `https://<votre-username>.github.io/basketball-analytics`

## Mettre à jour les données

L'application accepte le fichier `Basketball_Analyses_V2.xlsx` (ou tout fichier au même format).

**Format attendu :**
- Feuille nommée **SYNTHESE**
- En-têtes en ligne 3
- Données athlètes à partir de la ligne 4
- Colonnes dans l'ordre : N°, NOM, ÂGE, POIDS, CMJ Hauteur, CMJ Pmax, SJ Hauteur, SJ Pmax, Diff CMJ-SJ, Indice SSC, Squat, Squat/PDC, Test Australien, T-Test, VIFT, VO2max, % Masse adipeuse, puis 8 notes /10, puis Score Global

## Indicateurs mesurés

| Indicateur | Description |
|---|---|
| CMJ | Counter Movement Jump — saut avec élan |
| SJ | Squat Jump — saut depuis position statique |
| Diff CMJ-SJ | Différentiel (utilisation du cycle étirement-détente) |
| Indice SSC | Rapport CMJ/SJ (stretch-shortening cycle) |
| Squat / PDC | Force relative au poids de corps |
| Test Australien | Force isométrique des ischio-jambiers (N) |
| T-Test | Test d'agilité (secondes) |
| VIFT | Vitesse maximale au 30-15 IFT (km/h) |
| VO2max | Consommation max d'oxygène (ml/kg/min) |

## Technologies

- HTML / CSS / JavaScript pur (aucune dépendance locale)
- [Chart.js](https://www.chartjs.org/) — graphiques
- [SheetJS](https://sheetjs.com/) — lecture des fichiers Excel
