Voici la **version professionnelle en français**, optimisée pour un README GitHub technique, claire et adaptée aux recruteurs Data / BI :

---

# 📊 Modèle de Données Power BI — Documentation de Préparation & Transformation

##  Objectif du projet

Ce projet consiste à concevoir un **modèle sémantique propre, structuré et évolutif** dans Power BI, en appliquant les bonnes pratiques de transformation, modélisation et structuration des données.
L’objectif final est de fournir un jeu de données robuste prêt pour l’analyse avancée, les mesures DAX et les tableaux de bord interactifs.

---

## 1. Stratégie de préparation des données

Toutes les tables ont été transformées dans **Power Query** selon des standards BI professionnels :

* Convention de nommage des tables :

  * Tables de dimensions → `Dim*`
  * Table de faits → `FactSales`
* Normalisation des colonnes :

  * Clés substituts → `*Key`
  * snake_case → PascalCase
* Typage strict des données :

  * Clés → Nombre entier
  * Montants → Décimal
  * Dates → Date
  * Texte → Texte
* Suppression des doublons sur les clés de dimensions
* Gestion des valeurs nulles :

  * Attributs descriptifs → `"Unknown"`
  * Clés → aucune valeur nulle autorisée

---

## 2. Structure du modèle décisionnel

Le modèle suit une architecture **en étoile (Star Schema)**.

### Table de faits

* `FactSales` — données transactionnelles de ventes

### Tables de dimensions

* `DimCustomers`
* `DimProducts`
* `DimDates`
* `DimStores`
* `DimSalesperson`
* `DimCampaigns`

**Avantages de cette architecture :**

* Performance des requêtes optimisée
* Relations simplifiées
* Scalabilité du modèle
* Calculs DAX plus efficaces

---

## 3. Préparation spécifique par table

###  DimDates

* Conversion en type Date
* Suppression des doublons
* Définie comme table de dates officielle
* Activation des calculs Time Intelligence :

  * YTD
  * MTD
  * YoY
  * Same Period Last Year

---

###  DimCustomers

* Clé primaire nettoyée
* Attributs standardisés
* Colonne calculée possible : FullName
* Table prête pour relations

---

###  DimProducts

* Clé ProductKey validée
* Hiérarchie produits :
  **Catégorie → Marque → Produit**

---

###  DimStores

* Clé StoreKey validée
* Hiérarchie géographique :
  **Localisation → Type → Magasin**
* Catégorie géographique définie pour la cartographie

---

### DimSalesperson

* Clé primaire valide
* Structure simplifiée orientée analyse

---

###  FactSales

* Types numériques corrigés
* Colonne date standardisée
* Clés étrangères vérifiées
* Table centrale du modèle

---

## 4. Hiérarchies implémentées

Les hiérarchies permettent l’analyse hiérarchique et le drill-down :

* Date → Année → Trimestre → Mois → Jour
* Produit → Catégorie → Marque → Produit
* Magasin → Localisation → Type → Nom
* Client (optionnel) → Segment → Nom

---

## 5. Validation du modèle

Le modèle final respecte les critères qualité BI :

✔ Données nettoyées et standardisées
✔ Intégrité référentielle assurée
✔ Relations optimisées
✔ Table de dates configurée
✔ Hiérarchies créées
✔ Catégorisation géographique appliquée

---

## 🏁 Résultat final

Le dataset est désormais :

* prêt pour l’analyse
* optimisé en performance
* structuré et évolutif
* conforme aux standards BI

Il peut être utilisé immédiatement pour :

* Création de KPIs
* Mesures DAX avancées
* Tableaux de bord interactifs
* Reporting décisionnel

---

## 🔜 Prochaine étape du projet

Développements prévus :

* Implémentation des KPIs
* Définition des métriques métier
* Conception du dashboard analytique
* Visualisation d’insights



