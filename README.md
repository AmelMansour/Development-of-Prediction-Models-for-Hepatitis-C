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

# La méthode CRISP-DM
CRISP-DM est l'acronyme de Cross-Industry Standard Process for Data Mining (Processus Standard Inter-Industries pour l'Exploration de Données). Il s'agit d'un modèle de processus de gestion de projets d'exploration de données qui fournit une approche structurée pour la planification, la mise en œuvre et la maintenance de solutions d'exploration de données.
En adaptant cette méthodologie, on va expliquer les différents étapes basé dans mon script.
![image](https://github.com/AmelMansour/Develop-class-prediction-models-assess-performance-through-cross-validation-and-diverse-criteria/assets/141269604/4dcffcbf-8c0f-474a-8b95-90aa8b563575)

# Objectif du Projet : 
L'objectif principal de ce projet est d'appliquer diverses techniquesd'apprentissage automatique afin de réaliser l'apprentissage et la classification des enregistrements liés à la base de données du virus de l'hépatite C pour des patients égyptiens. Le but ultime est de développer des modèles de classification capables de prédire la classe de la variable cible
'Baselinehistological staging' en fonction d'autres caractéristiques médicales.

# Import des bibliothèques nécessaires:
![image](https://github.com/AmelMansour/Develop-class-prediction-models-assess-performance-through-cross-validation-and-diverse-criteria/assets/141269604/e3aa16cd-13e0-4ddb-9537-00f379cf0074)

# Phase 1: Compréhension du Métier (Business Understanding)
L'objectif commercial est de fournir des outils d'aide à la décision pour évaluer le stade histologique de l'hépatite C chez les patients égyptiens. Cela permettrait une meilleure compréhension de la progression de la maladie et une prise en charge médicale plus précise.
# Phase 2: Compréhension des Données (Data Understanding)
•Collecte des Données : Les données sont extraites de la base du virus de l'hépatite C pour des patients égyptiens « HCV-Egy-Data.csv »
•Exploration des Données : Analyse des caractéristiques disponibles, identification des classes de la variable cible, et compréhension des relations entre les différentes variables.

![image](https://github.com/AmelMansour/Develop-class-prediction-models-assess-performance-through-cross-validation-and-diverse-criteria/assets/141269604/f12a0940-1435-42b9-af2f-5fe97ca801f8)

[1385 rows x 29 columns]
J’ai un ensemble de données qui comprend 1385 lignes (ou observations) et 29 colonnes (ou variables). Cela signifie que chaque ligne dans votre ensemble de données représente une entrée ou une instance, et chaque colonne représente une caractéristique ou une variable différente associée à ces entrées.

# Phase 3: Préparation des Données (Data Preparation)
![image](https://github.com/AmelMansour/Develop-class-prediction-models-assess-performance-through-cross-validation-and-diverse-criteria/assets/141269604/3d9bfb09-a701-4858-a1cd-534d68dbc839)
![image](https://github.com/AmelMansour/Develop-class-prediction-models-assess-performance-through-cross-validation-and-diverse-criteria/assets/141269604/08d06530-a839-4a6b-b2bc-ab0274eb357e)

• Nettoyage des Données : Les valeurs 5 dans certaines colonnes sont remplacées par NaN, puis les valeurs aberrantes sont détectées et traitées.
• Imputation : Les valeurs manquantes sont imputées en utilisant la médiane.
• Standardisation / Normalisation : Les données sont standardisées pour s'assurer que toutes les caractéristiques ont la même échelle « StandardScaler / Scikit-learn »
• Sélection des caractéristiques : Identifier et conserver les caractéristiques les plus importantes en éliminant celles qui sont redondantes ou moins informatives « SelectKBest »
• Encodage des variables catégorielles : L'encodage des variables catégorielles consiste à convertir des variables qualitatives (catégorielles) en une forme numérique afin de pouvoir les utiliser comme entrées dans des modèles d'apprentissage automatique « LabelEncoder »
• Équilibrage des classes : Technique d'échantillonnage (Si les classes ne sont pas équilibrées) « Smote »

# Phase 4: Modélisation (Modeling)
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

# Phase 5: Évaluation (Evaluation)
![image](https://github.com/AmelMansour/Develop-class-prediction-models-assess-performance-through-cross-validation-and-diverse-criteria/assets/141269604/6c73918d-b123-48b9-aaf1-57c57f6f64c7)

•Évaluation des Modèles : Les résultats des modèles sont évalués pour chaque classe binaire.
•Comparaison des Performances : Les performances des modèles sont comparées et analyséespour chaque classe binaire.

# Phase6 :Déploiement (Deployment): 
Sauvegarde des modèles entraînés pour une utilisation future

# Analyse et Interprétation : 
• Classe Binaire 1.0
![image](https://github.com/AmelMansour/Develop-class-prediction-models-assess-performance-through-cross-validation-and-diverse-criteria/assets/141269604/2247839c-8f3b-4716-aa8a-e5b3bbff7fbd)

• Classe Binaire 2.0
![image](https://github.com/AmelMansour/Develop-class-prediction-models-assess-performance-through-cross-validation-and-diverse-criteria/assets/141269604/40306c26-49b4-4242-9920-ec19846f131d)

• Classe Binaire 3.0
![image](https://github.com/AmelMansour/Develop-class-prediction-models-assess-performance-through-cross-validation-and-diverse-criteria/assets/141269604/1e9210a1-af7b-4be1-bf95-253c73acf246)

• Classe Binaire 4.0
![image](https://github.com/AmelMansour/Develop-class-prediction-models-assess-performance-through-cross-validation-and-diverse-criteria/assets/141269604/19c980a7-4b55-4b6c-8d3f-c53c6ab27f35)

# Conclusion
# •Modèle de Classification :
* Classe binaire 1.0 :
Les performances des modèles sont relativement similaires, avec des valeurs autour de 60 %, indiquant une précision et un rappel moyens.
* Classe binaire 2.0 :
Le modèle d'amélioration du gradient a considérablement amélioré les performances, atteignant environ73 % en termes de précision, de rappel et de score F1. Les autres modèles fonctionnent entre 54 et 65 %.
* Classe binaire 3.0 :
Ces modèles ont des performances équilibrées avec des valeurs d'environ 54 à 56 % et ont une précision et un rappel similaires.
* Classe binaire 4.0 :
Random Forest et Gradient Boosting se caractérisent par des performances d'environ 66 à 67 %, tandis que d'autres modèles atteignent des valeurs modestes d'environ 53 à 56 %.

# •Matrice de confusion :
Une matrice de confusion est un tableau qui décrit les performances d'un modèle de classification sur un ensemble de données. Cela vous permet de visualiser le nombre de prédictions correctes et incorrectes de votre modèle. Les matrices de confusion sont particulièrement utiles pour évaluer les performances des modèles en classification binaire. La matrice de confusion est généralement construite comme suit
[[164 39]
[ 55 19]]
• 164 (en haut à gauche) : Vrais Négatifs (VN) - Il y a 164 instances correctement prédites comme négatives par le modèle. Ces sont des observations qui étaient négatives et ont été correctement classées comme telles.
• 39 (en haut à droite) : Faux Positifs (FP) - Il y a 39 instances qui ont été prédites comme positives par le modèle, mais qui étaient en réalité négatives. Ces sont des erreurs de type I, où le modèle a erronément prédit une occurrence positive.
• 55 (en bas à gauche) : Faux Négatifs (FN) - Il y a 55 instances qui ont été prédites comme négatives par le modèle, mais qui étaient en réalité positives. Ces sont des erreurs de type II, où le modèle a manqué des occurrences positives.
• 19 (en bas à droite) : Vrais Positifs (VP) - Il y a 19 instances correctement prédites comme positives par le modèle. Ces sont des observations qui étaient positives et ont été correctement classées comme telles.

➔La Visualisation de la matrice de confusion sous forme de carte thermique nous aide à comprendre les erreurs du modèle. Les valeurs sont numérotées pour indiquer la fréquence à laquelle chaque catégorie apparaît, et les couleurs peuvent être utilisées pour mettre en évidence les différences (par exemple, les vrais positifs peuvent être colorés en vert, les faux positifs en rouge, etc.).
Dans le contexte des matrices de confusion et de la visualisation des couleurs, différentes couleurs peuvent être utilisées pour représenter différentes catégories dans la matrice de confusion. Cependant, les couleurs spécifiques peuvent varier en fonction de la palette de couleurs utilisée. Généralement, dans une matrice de confusion, vous pouvez attribuer des couleurs à des éléments spécifiques comme ceci :
Exploiter la Validation Croisée pour Appliquer Diverses Méthodes de Classification sur l'Ensemble
de Données Initial et Évaluer Leurs Performances Selon Divers Critères
*Vrai positif : souvent affiché en vert ou en bleu, indiquant que le modèle a correctement prédit un cas positif.
*Vrai négatif : souvent affiché en vert ou en bleu, indiquant que le modèle a correctement prédit un cas négatif.
*Faux positif : souvent affiché en rouge ou en jaune, il indique que le modèle a prédit à tort le cas comme étant positif.
*Faux négatif : souvent affiché en rouge ou en jaune, il indique que le modèle a prédit à tort le cas comme étant négatif.

➔En résumé, le modèle Random Forest atteint des performances cohérentes sur toutes les mesures et montre une capacité équilibrée à prédire correctement les classes positives et négatives.


