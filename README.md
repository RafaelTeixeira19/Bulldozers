# Prévision du prix de vente de Bulldozers

Le but de ce projet est de prévoir le prix de vente aux enchères de Bulldozers. La question à laquelle il est nécessaire de répondre est la suivante :
> Dans quelles mesures peut-on prévoir le prix de vente d'un bulldozer compte tenu de ses caractéristiques et de l'historique de ventes des anciens bulldozers ?

## Résumé de la démarche
La réalisation du projet est faite dans Jupyter Notebook grâce au langage Python. Tout d'abord, une analyse de données exploratoire (EDA) est réalisée grâce aux packages Matplotlib, Pandas et Numpy. Celle-ci a permis d'observer que la variable "date de vente" n'est pas au bon format. Elle a donc été corrigée et une création de variables supplémentaires a eu lieu, ceci afin de rendre la prédiction du modèle plus précise. 

Par ailleurs, la base de données contenait un nombre conséquent de valeurs NaN et de variables au mauvais format. La seconde étape a donc été de les traiter au cas par cas afin de ne pas rendre le prédictions du modèle fausses. La troisième étape consitait à mettre les variables au bon format afin de pouvoir entraîner le modèle et faire des prédictions. 

Enfin, la création du modèle et la prédiction du prix de vente ont été effectuées. Tout d'abord, la base de données a été divisée en deux échantillons : celui d'entraînement et celui de validation. Le modèle importé à partir de Scikit-learn est le "RandomForestRegressor". Ce modèle permet d'avoir les avantages d'un "RandomForest" et de l'adapter à des problèmes de prédiction de valeurs linéaires plutôt que de classification. Il a ensuite été entraîné sur l'échantillon adéquat. Un ajustement des paramètres s'est fait via une validation croisée par recherche aléatoire. Enfin, une prédiction a eu lieu sur l'échantillon de validation. 

## Résultats
#### Echantillon test
* Coefficient de détermination (R²) = 0.96
* Erreur moyenne absolue (MAE) = $2953
* Erreur logarithmique quadratique moyenne (RMSLE) = 0.145 

#### Echantillon de validation 
* Coefficient de détermination (R²) = 0.88
* Erreur moyenne absolue (MAE) = $5951
* Erreur logarithmique quadratique moyenne (RMSLE) = 0.245
