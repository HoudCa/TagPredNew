# Qu'est que Stack Overflow ?
Stack Overflow est la communauté en ligne la plus grande et la plus fiable permettant aux développeurs d'apprendre, de partager leurs connaissances en programmation.
Le site Web sert de plate-forme aux utilisateurs pour poser et répondre à des questions d'une manière similaire à un wiki ou à Digg. 
# Définition du problème 
Étant donné un titre et le corps d'une question, nous devons prédire les balises pertinentes de sorte que la question soit recommandée au bon domaine afin que l'expert puisse répondre correctement à la question.
Pour cela, nous devrions obtenir une précision et des taux de rappel élevés. C'est-à-dire que nous devons être vraiment sûrs que la balise prédite appartient à la question donnée. De plus, nous voulons avoir un taux de rappel élevé, ce qui signifie que si la balise est réellement censée être présente, nous voulons qu'elle soit présente le plus souvent.
# Données
Les données se composent de 6 colonnes:

1- Id : Représente l'ID de la question
2- Titre : Représente le titre de la question
3- Corps : Représente le corps de la question où la question est expliquée correctement
4- Balises : Les balises pertinentes pour la question posée
5- CreationDate : La date à laquelle la question a été posée
6- Type : Traite de la qualité de la question.

Nos principales caractéristiques importantes dans l'ensemble de données sont Title, Bodyet Tags.

# Modélisation en problème de machine learning
Puisque nous comprenons bien le problème métier, essayons de le poser comme un véritable problème d'apprentissage automatique.
Noua allons utilisé 2 approches :
## Approche non supervisée : ** un modèle LDA à l'aide d'un corpus Gensim ** 

* Le modèle LDA utilise des méthodes de classification probabilistes pour affecter chaque question à un ou plusieurs topics.
* Feature engineering : Bag-of-words
 * Matrice de fréquence des termes dans les questions : chaque mot de la question est associé à un identifiant et la fréquence d’apparition de chacun des termes est calculé dans une matrice.
* Détermination des “Topics” qui seront dans notre cas un ensemble de tags, puis affecter un topic aux question.

## Approche supervisée : Problème de classification multilabels
* Feature extraction avec TF-IDF :
  * Regression logistique avec OneVsRest Classifier
  * Une descente de gradient stochastique (SGDC) avec OneVsRest Classifier
* Feature extraction Word2VEC, USE et BERT :
  * Regression logistique avec OneVsRest Classifier
  * Une descente de gradient stochastique (SGDC) avec OneVsRest Classifier
 ## Déploiement de l'application
Notre application est écrite avec Python à l'aide du framework Flask, puis déployée sur Heroku









