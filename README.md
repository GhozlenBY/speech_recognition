# Projet de Reconnaissance Vocale avec Edge Impulse et Arduino Nano 33 BLE Sense
![image](https://github.com/GhozlenBY/speech_recognition/assets/148441001/ae94712c-f683-42c2-bc2a-6ec5316f91ac)

# Description
Ce projet implémente un modèle d'apprentissage automatique pour la reconnaissance de mots-clés (Red, Green, Yellow) à l'aide de l'Arduino Nano 33 BLE Sense et Edge Impulse.

# Contexte et Objectifs
Nous avons entrepris ce projet pour explorer les capacités de l'apprentissage automatique dans le domaine de la reconnaissance vocale. En utilisant un microcontrôleur comme l'Arduino Nano 33 BLE Sense, nous avons cherché à développer un modèle capable de détecter et de répondre à des commandes vocales spécifiques.

# Matériel et Logiciel Utilisés
• Matériel : Arduino Nano 33 BLE Sense.
• Logiciels : Edge Impulse CLI, Arduino CLI.
• Téléphone protable ou ordinateur

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
![Data](https://github.com/GhozlenBY/speech_recognition/assets/148441001/4e5412f1-0099-49ea-a406-12312e76cb85)


5. Création de l'Impulsion
• Ajout d'un bloc de traitement audio et d'un bloc d'apprentissage dans Edge Impulse.
![impulse](https://github.com/GhozlenBY/speech_recognition/assets/148441001/4768ef4a-c84d-4508-aa21-b32e24e9a727)

• Génération des caractéristiques des données collectées.

6. Entraînement et Validation du Modèle
• génération des features
 ![features](https://github.com/GhozlenBY/speech_recognition/assets/148441001/fe58794a-d11b-4c22-998f-f3e2e3bde24b)

• Utilisation de l'outil NN Classifier d'Edge Impulse pour l'entraînement du modèle.

• Évaluation des performances du modèle et ajustements si nécessaire pour atteindre une haute précision.

![Model](https://github.com/GhozlenBY/speech_recognition/assets/148441001/eeaecdf2-b814-4672-a057-1854a27be283)

7. Déploiement et Test du Modèle
• Compilation et exportation du modèle entraîné sous forme de bibliothèque Arduino.

• Test du modèle en temps réel avec l'Arduino Nano 33 BLE Sense ou avec un téléphone en scannant le code QR sut la fenètre deployment.

# Résultats et Observations
• Le modèle a montré une capacité élevée à reconnaître les mots-clés spécifiés.

• La précision globale du modèle était satisfaisante, avec peu de fausses détections ou de manquements parfois mais golobalement les model a réussi à identifier les couleurs avec avec des pourcentages acceptables.
![image_123986672 (3)](https://github.com/GhozlenBY/speech_recognition/assets/148441001/627ca0f0-a955-44dc-a0df-ba981f0b1d0e)
![image_123986672 (4)](https://github.com/GhozlenBY/speech_recognition/assets/148441001/dfe0413b-b9ac-41ef-bfd7-f6742f8c2608)
![image_123986672 (5)](https://github.com/GhozlenBY/speech_recognition/assets/148441001/6fbf9abc-810c-463e-9e85-afa74ea7bf02)
![unnamed](https://github.com/GhozlenBY/speech_recognition/assets/148441001/4a1c1187-75f1-4f0a-9961-b485ae64de6f)



