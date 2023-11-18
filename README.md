# Projet de Reconnaissance Vocale avec Edge Impulse et Arduino Nano 33 BLE Sense

# Description
Ce projet implémente un modèle d'apprentissage automatique pour la reconnaissance de mots-clés (Red, Green, Yellow) à l'aide de l'Arduino Nano 33 BLE Sense et Edge Impulse.

# Contexte et Objectifs
Nous avons entrepris ce projet pour explorer les capacités de l'apprentissage automatique dans le domaine de la reconnaissance vocale. En utilisant un microcontrôleur comme l'Arduino Nano 33 BLE Sense, nous avons cherché à développer un modèle capable de détecter et de répondre à des commandes vocales spécifiques.

# Matériel et Logiciel Utilisés
• Matériel : Arduino Nano 33 BLE Sense.
• Logiciels : Edge Impulse CLI, Arduino CLI.

#Étapes de Développement

1. Préparation de l'Environnement de Travail
• Installation des CLI nécessaires.
• Mise à jour du firmware de l'Arduino Nano 33 BLE Sense pour la compatibilité avec Edge Impulse.

2. Connexion et Configuration de la Carte
• Connexion de l'Arduino Nano 33 BLE Sense à Edge Impulse via le terminal.
• Création du projet speech_recognition dans Edge Impulse.

4. Collecte et Traitement des Données
• Enregistrement de plusieurs échantillons pour chaque mot-clé (rouge, vert, jaune) et pour le bruit de fond.
• Configuration du microphone intégré pour une durée d'échantillonnage de 2500 ms à une fréquence de 16 000 Hz.
• Pour chaque label (couleur), nous avons enregistré des échantillons d'une durée totale de 1,12 minute afin d'obtenir un volume de données suffisant pour un entraînement efficace du modèle. De plus, une durée équivalente de 1,12 minute de silence (noise) a été enregistrée pour entraîner le modèle à reconnaître les moments de non-parole.
![alt tag](https://github.com/GhozlenBY/speech_recognition/issues/1#issue-2000572186)

5. Création de l'Impulsion
• Ajout d'un bloc de traitement audio et d'un bloc d'apprentissage dans Edge Impulse.
![alt tag](https://github.com/GhozlenBY/speech_recognition/issues/3#issue-2000574470)
• Génération des caractéristiques des données collectées.

6. Entraînement et Validation du Modèle
• génération des features
 ![alt tag](https://github.com/GhozlenBY/speech_recognition/issues/2#issue-2000573876)
• Utilisation de l'outil NN Classifier d'Edge Impulse pour l'entraînement du modèle.
• Évaluation des performances du modèle et ajustements si nécessaire pour atteindre une haute précision.
![alt tag](https://github.com/GhozlenBY/speech_recognition/issues/4#issue-2000574759)

7. Déploiement et Test du Modèle
• Compilation et exportation du modèle entraîné sous forme de bibliothèque Arduino.
• Test du modèle en temps réel avec l'Arduino Nano 33 BLE Sense ou avec un téléphone en scannant le code QR sut la fenètre deployment.

# Résultats et Observations
• Le modèle a montré une capacité élevée à reconnaître les mots-clés spécifiés.
• La précision globale du modèle était satisfaisante, avec peu de fausses détections ou de manquements( comme ci-dessous).
![alt tag](https://github.com/GhozlenBY/speech_recognition/issues/8#issue-2000575488)
![alt tag](https://github.com/GhozlenBY/speech_recognition/issues/7#issue-2000575398)
![alt tag](https://github.com/GhozlenBY/speech_recognition/issues/6#issue-2000575305)
![alt tag](https://github.com/GhozlenBY/speech_recognition/issues/5#issue-2000575208)

