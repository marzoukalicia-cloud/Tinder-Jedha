# Tinder-Jedha
Tinder - Speed Dating Analysis - Bloc 2 Exploratory Data Analysis - Jedha Bootcamp

## 🎯 Contexte & Objectif Métier
L'équipe marketing de **Tinder** constate une baisse globale du nombre de *matches* sur l'application[cite: 8]. Pour y remédier, une expérience sociologique de Speed Dating de grande envergure (4 minutes par rencontre) a été menée afin de collecter des données démographiques, psychologiques et comportementales sur les participants[cite: 8, 11]. 

L'objectif de ce projet est de mener une **Analyse Exploratoire de Données (EDA)** approfondie pour décrypter les dynamiques de l'attraction et comprendre **ce qui pousse scientifiquement deux individus à vouloir se revoir** pour un second rendez-vous[cite: 8].

---

## 🛠️ Clés du Preprocessing & Rigueur Méthodologique
* **Dédoublonnement des profils :** Les données d'origine répètent les caractéristiques des participants à chaque rencontre[cite: 8]. Un sous-jeu de données `profiles` unique a été isolé par `iid` afin de ne pas fausser les analyses statistiques démographiques[cite: 11].
* **Harmonisation des Échelles (Vagues 6 à 9) :** Correction d'une anomalie majeure du dataset d'origine où certaines vagues notaient les critères sur une échelle de 1 à 10 et d'autres par allocation de 100 points[cite: 10]. Un script de normalisation a été appliqué pour remettre l'intégralité du scope sur une base 100[cite: 10].

---

## 📈 Enseignements Clés & Réponses aux Problématiques

### 1. Attentes déclarées selon le genre (Heatmap)
* **Hommes :** La **Beauté physique (56.6 points)** est le critère ultra-dominant, reléguant l'ambition et les intérêts communs au second plan.
* **Femmes :** Les attentes sont beaucoup plus homogènes et sélectives, plaçant l'**Intelligence (51.8 points)** et la **Sincérité (48.8 points)** au-dessus du simple critère esthétique.

### 2. L'impact réel de l'Attractivité (Boxplots)
* Il existe un paradoxe entre le déclaratif et le comportement réel. L'analyse des décisions montre que l'attractivité physique perçue est le véritable juge de paix : la note médiane attribuée passe de **6/10 pour un refus** à **7/10 minimum pour déclencher un Match**.

### 3. Origine culturelle vs Centres d'intérêt commune
* Contrairement aux idées reçues, partager la même origine ethnique (`samerace`) n'augmente le taux de match que de **1%** (17.1% vs 16.1%). L'ouverture géosociale et les affinités réelles prédominent largement sur les barrières communautaires.

### 4. Effet de position et Fatigue Cognitive (Lineplot)
* Le premier rendez-vous de la soirée bénéficie d'un taux d'acceptation de **50%**. On observe ensuite une chute linéaire au fil des rendez-vous (point bas à 33%). Les analyses prouvent que ce n'est pas la qualité des partenaires qui décline, mais la fatigue cognitive des utilisateurs qui deviennent de plus en plus sélectifs et distants à mesure que les rendez-vous s'enchaînent.

---

## 📂 Structure du Répertoire GitHub

```text
📦 Tinder-Jedha
 ┣ 📂 notebook
 ┃ ┗ 📜 3.Projet_Tinder_Final.ipynb   # Analyses statistiques, nettoyage des vagues et visualisations Plotly
 ┣ 📂 data
 ┃   ┣ 📜 Speed+Dating+Data+Key.doc   # Dictionnaire complet des variables et guide des métriques originales
 ┃   ┗ 📜 Speed+Dating+Data.csv       # Échantillon extrait du jeu de données source
 ┣ 📂 outputs
 ┃   ┣ 📜 heatmap_gender.png         # Matrice d'importance des critères déclarés (Hommes vs Femmes)
 ┃   ┣ 📜 Q0_1.png                   # Distribution des âges par genre (Boxplot de détection des outliers)
 ┃   ┣ 📜 Q0_2.png                   # Pyramide des âges globale de la population (Histogramme de densité)
 ┃   ┣ 📜 Q0_3.png                   # Analyse de la structure de l'échantillon par vague d'expérience
 ┃   ┣ 📜 Q0_5.png                   # Répartition des participants selon leur domaine d'étude principal
 ┃   ┣ 📜 Q2_1.png                   # Importance déclarée de l'attractivité physique vs les autres critères
 ┃   ┣ 📜 Q2_1_boxplot.png           # Variabilité des notes d'attraction globale distribuées par genre
 ┃   ┣ 📜 Q2_2.png                   # Nuage de points : Note de beauté reçue vs Probabilité de succès estimée
 ┃   ┣ 📜 Q2_2_boxplot.png           # Impact réel de l'attractivité physique sur la validation du Match
 ┃   ┣ 📜 Q3_1.png                   # Graphique en barres : Impact d'une origine ethnique commune (samerace) sur le Match
 ┃   ┣ 📜 Q3_2_boxplot.png           # Impact de la corrélation des intérêts partagés sur la décision positive
 ┃   ┣ 📜 Q3_4.png                   # Analyse sémantique de l'importance accordée aux centres d'intérêt communs
 ┃   ┣ 📜 Q3_5_boxplot.png           # Corrélation entre la conformité culturelle et le taux de transformation
 ┃   ┣ 📜 Q4.png                     # Nuage de points : Confrontation entre l'auto-évaluation et la note réelle reçue
 ┃   ┣ 📜 Q5_2.png                   # Courbe d'évolution du taux de décision positive au fil de la soirée (Order)
 ┃   ┗ 📜 Q5_boxplot.png             # Boxplots de mesure de la fatigue cognitive et de la sévérité des notes
 ┗ 📜 README.md                      # Synthèse méthodologique, insights stratégiques et recommandations produit

👨‍💻 Auteur
Projet d'Analyse Exploratoire conçu et réalisé par Alicia Marzouk dans le cadre de la certification du Bloc #2 — Exploratory Data Analysis, Jedha Bootcam
