# Prédiction de balise de débordement de pile 🏷️
Un modèle d'apprentissage automatique qui prédit les balises pour une question et un corps donnés


# Pour les développeurs, par les développeurs 👨‍💻
Stack Overflow est une communauté ouverte à tous ceux qui codent. Ils vous permettent d'obtenir des réponses à vos questions de codage les plus difficiles, à partager vos connaissances avec vos collègues en privé et à trouver votre prochain emploi de rêve.

# Pour les entreprises, par les développeurs 🕴️
Leur mission est d'aider les développeurs à écrire le script du futur. Cela signifie vous aider à trouver et à embaucher des développeurs qualifiés pour votre entreprise et leur fournir les outils dont ils ont besoin pour partager leurs connaissances et travailler efficacement.

# Définition du problème 🤔
Étant donné un titre et le corps d'une question, nous devons prédire les balises pertinentes de sorte que la question soit recommandée au bon domaine expertafin que l'expert puisse répondre correctement à la question.

# Contraintes commerciales ✔️
 • Pour prédire autant de balises que possible avec des precisionet très élevés recall.
 • Incorrect tagspourrait avoir un impact customer experiencesur Stack Overflow.
 • Aucune contrainte de latence stricte. Le modèle doit pouvoir générer les balises pertinentes dans une quantité de temps raisonnable.

# Données 🗄️
 • train.csv= 48 Mo
 • test.csv= 16 Mo
Les données se composent de 6 colonnes:

1- Id : Représente l'ID de la question
2- Titre : Représente le titre de la question
3- Corps : Représente le corps de la question où la question est expliquée correctement
4- Balises : Les balises pertinentes pour la question posée
5- CreationDate : La date à laquelle la question a été posée
6- Type : Traite de la qualité de la question.

Nos principales caractéristiques importantes dans l'ensemble de données sont Title, Bodyet Tags.

# Des parcelles pour mieux comprendre 📊

# Countplot de balises par question 📈

Il s'agit du décompte du nombre de balises par question


La clé à retenir de l'intrigue ci-dessus est que la plupart des questions contiennent 2des 3balises.

# Répartition des balises 📉
Il s'agit de la distribution du nombre de fois que le tag est apparu dans les questions






