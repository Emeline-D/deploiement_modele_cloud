# Déploiement d'un modèle dans le cloud.

Ce projet est le dernier du parcours d'OpenClassrooms, à savoir le déploiement d'un modèle dans le cloud. Ainsi, nous allons déployer un modèle de réduction de dimensions sur des images de fruits sur AWS, dans le but de pouvoir traiter un nombre très important d'images sans faire face à des limitations.

Pour ce faire, nous utilisons donc une architecture de calculs distribués, composée de :
- Un espace de stockage S3 contenant les différentes images du projet réparties en 3 dossiers : Traning, Test, et multiple_test-fruits. Ici, pour entraîner le modèle, nous nous servirons exclusivement des images Test.
-Un serveur de calculs EC2 qui permettra d'exécuter notre modèle, et lié au S3 grâce à Hadoop. Ici, nous avons choisi une instance payante, mais de petite taille, à savoir t2.xlarge, pour à la fois faire tourner rapidement notre modèle, mais également prévoir un peu de marge avec l'augmentation future du nombre d'images. Ce serveur contient les librairies Java 8, python 3.6, pip pour python3, numpy, pandas, jupyter, tensorflow 2.1.0, pyarrow 0.13, Spark 2.4.5 et Hadoop 2.7.3.

Données disponibles ici : https://www.kaggle.com/moltean/fruits
