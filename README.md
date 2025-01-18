# Prédiction du prix de vente de Bulldozers

Le but de ce projet était de prédire le prix de vente aux enchères de Bulldozers. La question à laquelle il fallait répondre était la suivante :
> Dans quelles mesures peut-on prédire le prix de vente d'un bulldozer, compte tenu de ses caractéristiques et de l'historique de ventes des anciens bulldozers ?

## Résumé de la démarche
La réalisation du projet a été faite dans Jupyter Notebook grâce au language Python. Tout d'abord, une analyse de données exploratoire (EDA) a été faite grâce au packages Matplotlib, Pandas et Numpy. Celle-ci a permit d'observer que la variable date de vente n'était pas au bon format. Elle a été corrigée et une création de variables supplémentaires a eu lieu. Ceci dans le but de rendre la prédiction du modèle plus précise. 

Ensuite, la base de données contenait énormément de valeurs NaN et les mauvais formats de variables. La deuxième étape a donc été de les traiter au cas par cas afin de ne pas rendre le prédictions du modèle fausses. La troisième étape a été de mettre les variables au bon format afin de pouvoir entrainer le modèle et faire des prédictions. 

Enfin, la création du modèle et la prédiction du prix de vente a été effectué. D'abord la base de données a été divisée en deux échantillons, celui d'entraînement et celui de validation. Le modèle mporté à partir de Scikit-learn a été le "RandomForestRegressor". Celui-ci permet d'avoir la précision d'un arbre de précision mais l'adapter à des problèmes de prédiction de valeurs linéaires plutôt que de classification. Le modèle a été ensuité entrainé sur l'échantillon adéquat. Un ajustement des paramètres a eu lieu via une validation croisée par recherche aléatoire. Enfin, une prédiction a eu lieu sur l'échantillon de validation. 

## Résultats
#### Echantillon test
Coefficient de détermination (R²) = 0.96
Erreur moyenne absolue (MAE) = $2953
Erreur logarithmique quadratique moyenne (RMSLE) = 0.145 

#### Echantillon de validation 
Coefficient de détermination (R²) = 0.88
Erreur moyenne absolue (MAE) = $5951
Erreur logarithmique quadratique moyenne (RMSLE) = 0.245
