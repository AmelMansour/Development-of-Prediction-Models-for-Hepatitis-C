# Develop-class-prediction-models-assess-performance-through-cross-validation-and-diverse-criteria

Ce projet est intéressant et potentiellement très bénéfique pour la santé publique, étant donné l'importance de la lutte contre le virus de l'hépatite C chez la population égyptienne . En effet , L’Égypte est le pays qui connaît l’épidémie d’hépatite C la plus importante au monde. S selon un communiqué publié sur le site Internet de l'OMS , il a diagnostiqué 87% des personnes vivant avec l'hépatite C qui est une infection du foie d’origine virale principalement transmise par le sang . 

Pour mener à bien ce projet, voici quelques étapes que vous pourriez envisager : 

1. Collecte des données : Rassemblez un ensemble de données représentatif des enregistrements relatifs à la base du virus de l'hépatite C pour des patients égyptiens.
2. Prétraitement des données : Nettoyez et préparez les données pour les rendre compatibles avec les modèles d'apprentissage automatique. Cela peut impliquer le traitement des valeurs manquantes, la normalisation des données, la gestion des outliers, etc.
3. Exploration des données : Effectuez une analyse exploratoire des données pour comprendre les relations entre les différentes variables. Cela pourrait vous aider à choisir les meilleures fonctionnalités pour votre modèle.
4. Choix des modèles : Sélectionnez différentes méthodes d'apprentissage automatique adaptées à la tâche de classification. Les méthodes couramment utilisées incluent les machines à vecteurs de support (SVM), les réseaux de neurones, les arbres de décision, et les méthodes ensemblistes comme les forêts aléatoires.
5. Divisez les données : Séparez vos données en ensembles d'entraînement et de test. Cela permet d'évaluer la performance de votre modèle sur des données qu'il n'a pas vues pendant l'entraînement.
6. Entraînement des modèles : Entraînez vos modèles à l'aide de l'ensemble d'entraînement. Utilisez des techniques de validation croisée pour évaluer la performance de manière robuste.
7. Évaluation des performances : Évaluez les performances de chaque modèle à l'aide de l'ensemble de test. Utilisez des métriques appropriées telles que la précision, le rappel, la F-mesure, etc.
8. Interprétation des résultats : Comprenez les décisions prises par votre modèle. Cela peut être crucial dans le domaine médical pour garantir la confiance des praticiens et des patients.
9. Déploiement : Une fois que vous êtes satisfait des performances de votre modèle, vous pouvez le déployer dans un environnement réel pour une utilisation pratique.

10. La méthode CRISP-DM. CRISP-DM est l'acronyme de Cross-Industry Standard Process for Data Mining (Processus Standard Inter-Industries pour l'Exploration de Données). Il s'agit d'un modèle de processus de gestion de projets d'exploration de données qui fournit une approche structurée pour la planification, la mise en œuvre et la maintenance de solutions d'exploration de données.
11. En adaptant cette méthodologie, on va expliquer les différents étapes basé dans mon script.
12. ![image](https://github.com/AmelMansour/Develop-class-prediction-models-assess-performance-through-cross-validation-and-diverse-criteria/assets/141269604/4dcffcbf-8c0f-474a-8b95-90aa8b563575)

13. Objectif du Projet : L'objectif principal de ce projet est d'appliquer diverses techniquesd'apprentissage automatique afin de réaliser l'apprentissage et la classification des enregistrements liés à la base de données du virus de l'hépatite C pour des patients égyptiens. Le but ultime est de développer des modèles de classification capables de prédire la classe de la variable cible
'Baselinehistological staging' en fonction d'autres caractéristiques médicales.

* Import des bibliothèques nécessaires:
![image](https://github.com/AmelMansour/Develop-class-prediction-models-assess-performance-through-cross-validation-and-diverse-criteria/assets/141269604/e3aa16cd-13e0-4ddb-9537-00f379cf0074)

* Phase 1: Compréhension du Métier (Business Understanding)
L'objectif commercial est de fournir des outils d'aide à la décision pour évaluer le stade histologique de l'hépatite C chez les patients égyptiens. Cela permettrait une meilleure compréhension de la progression de la maladie et une prise en charge médicale plus précise.
Phase 2: Compréhension des Données (Data Understanding)
•Collecte des Données : Les données sont extraites de la base du virus de l'hépatite C pour des patients égyptiens « HCV-Egy-Data.csv »
•Exploration des Données : Analyse des caractéristiques disponibles, identification des classes de la variable cible, et compréhension des relations entre les différentes variables.

![image](https://github.com/AmelMansour/Develop-class-prediction-models-assess-performance-through-cross-validation-and-diverse-criteria/assets/141269604/f12a0940-1435-42b9-af2f-5fe97ca801f8)

[1385 rows x 29 columns]
J’ai un ensemble de données qui comprend 1385 lignes (ou observations) et 29 colonnes (ou variables). Cela signifie que chaque ligne dans votre ensemble de données représente une entrée ou une instance, et chaque colonne représente une caractéristique ou une variable différente associée à ces entrées.

* Phase 3: Préparation des Données (Data Preparation)
![image](https://github.com/AmelMansour/Develop-class-prediction-models-assess-performance-through-cross-validation-and-diverse-criteria/assets/141269604/3d9bfb09-a701-4858-a1cd-534d68dbc839)
![image](https://github.com/AmelMansour/Develop-class-prediction-models-assess-performance-through-cross-validation-and-diverse-criteria/assets/141269604/08d06530-a839-4a6b-b2bc-ab0274eb357e)

• Nettoyage des Données : Les valeurs 5 dans certaines colonnes sont remplacées par NaN, puis les valeurs aberrantes sont détectées et traitées.
• Imputation : Les valeurs manquantes sont imputées en utilisant la médiane.
• Standardisation / Normalisation : Les données sont standardisées pour s'assurer que toutes les caractéristiques ont la même échelle « StandardScaler / Scikit-learn »
• Sélection des caractéristiques : Identifier et conserver les caractéristiques les plus importantes en éliminant celles qui sont redondantes ou moins informatives « SelectKBest »
• Encodage des variables catégorielles : L'encodage des variables catégorielles consiste à convertir des variables qualitatives (catégorielles) en une forme numérique afin de pouvoir les utiliser comme entrées dans des modèles d'apprentissage automatique « LabelEncoder »
• Équilibrage des classes : Technique d'échantillonnage (Si les classes ne sont pas équilibrées) « Smote »

* Phase 4: Modélisation (Modeling)
![image](https://github.com/AmelMansour/Develop-class-prediction-models-assess-performance-through-cross-validation-and-diverse-criteria/assets/141269604/b9bcd842-1681-492b-a84a-89147eed4c1b)
![image](https://github.com/AmelMansour/Develop-class-prediction-models-assess-performance-through-cross-validation-and-diverse-criteria/assets/141269604/57c15c46-1241-4372-a336-907967eeefb0)

• Création de Modèles : Sept modèles de classification sont utilisés:
✓ RandomForest
✓ SVM
✓ Logistic Regression
✓ Gradient Boosting
✓ Decision Tree
✓ K-Nearest Neighbors
✓ Naive Bayes
• Validation Croisée : La performance des modèles est évaluée en utilisant la validation croisée
avec des métriques telles que
✓ Accuracy
✓ Precision
✓ Rappel
✓ F1-score
✓ K-fold

Phase 5: Évaluation (Evaluation)
![image](https://github.com/AmelMansour/Develop-class-prediction-models-assess-performance-through-cross-validation-and-diverse-criteria/assets/141269604/6c73918d-b123-48b9-aaf1-57c57f6f64c7)

•Évaluation des Modèles : Les résultats des modèles sont évalués pour chaque classe binaire.
•Comparaison des Performances : Les performances des modèles sont comparées et analysées
pour chaque classe binaire.

* Phase6 :Déploiement (Deployment): Sauvegarde des modèles entraînés pour une utilisation future

# Analyse et Interprétation : 

