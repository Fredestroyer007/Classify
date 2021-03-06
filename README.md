# Classify : Classification musicale par apprentissage profond

Application de classification par apprentissage profond pour mon projet d'intégration au Collège de Bois-de-Boulogne à la session d'hiver 2020

## Description du projet

### L'idée

Le but de ce projet est de développer une application qui permet à l'utilisateur d'enregistrer ou téléverser un extrait d'une chanson et d'obtenir en retour le résultat du genre musical (pop, rock, classique, ...) de cet extrait.

### L'utilité et l'inovation

En dehors du domaine de la recherche, aucune solution existe qui permet à un utilisateur d'obtenir le genre musical d'une chanson par apprentissage profond. Les solutions existantes comme [Shazam](https://www.shazam.com/) compare l'empreinte du fichier audio à leur banque de données pour obtenir la classification du genre musical qui a été effectué par humain. L'approche proposée dans le cadre de ce projet permet de retirer l'humain de boucle et de permettre la classification de genre musical sans une banque de données préexistente.

### Lien avec d'autres matières

## État de la recherche

## Technologies

### Approche

Un modèle d'apprentissage profond qui classifie le genre musical sera développé à partir de la base de données [FMA](https://github.com/mdeff/fma) en utilisant la librarie [Fastai](https://docs.fast.ai/) pour pouvoir effectuer de l'apprentissage profond par transfert. Les différents extraits musicaux seront convertis en image sous forme de spectrogramme avec la librairie [LibROSA](https://librosa.github.io/librosa/) pour diminuer la quantité de données que les réseaux de neurones profonds doivent gérer. L'entraînement sera effectué dans [Google Colab](https://colab.research.google.com/notebooks/welcome.ipynb) pour profiter de la puissance de calcul gratuit. Le tout est stocké sur [Google Drive](https://drive.google.com/open?id=1gYMU7kj2xQS_sxeDPkipPwhLsI2V-Lgu) pour avoir accès à de la persistance dans [Google Colab](https://colab.research.google.com/notebooks/welcome.ipynb). Une fois le modèle peaufiné, il sera exporté par une opération Pickle de la librairie [Scikit-learn](https://scikit-learn.org/stable/). En utilisant [Starlette](https://www.starlette.io/), un script en Python sera développé pour permettre le prétraitement des données et l'inférence du modèle. Ce script sera déployé dans un contenant [Docker](https://www.docker.com/) sur le nuage.<br><br>
Pour l'application, elle sera développée avec [Flutter](https://flutter.dev/). Elle va inclure un API avec [Node.js](https://nodejs.org/en/) pour communiquer avec une base de données [MariaDB](https://mariadb.org/) pour permettre l'identification de l'utilisateur. L'application va aussi communiquer avec le contenant [Docker](https://www.docker.com/) du modèle d'apprentissage profond pour permettre le traitement des fichiers audios.

### Défi


### Bâtit avec

* [Python](https://www.python.org/) - Langage de programmation pour l'apprentissage profond
* [Dart](https://dart.dev/) - Langage de programmation pour le développement mobile
* [Flutter](https://flutter.dev/) - Kit de développement mobile
* [Node.js](https://nodejs.org/en/) - Librairie Javascript
* [MariaDB](https://mariadb.org/) - Programme de base de données
* [Docker](https://www.docker.com/) - Déploiement de conteneur
* [Fastai](https://docs.fast.ai/) - Librairie bâtit sur [PyTorch](https://pytorch.org/) pour l'apprentissage profond en Python
* [Scikit-learn](https://scikit-learn.org/stable/) - Libraire pour apprentissage machine en Python
* [Matplotlib](https://matplotlib.org/) - Libraire de traçage en Python
* [LibROSA](https://librosa.github.io/librosa/) - Libraire de traitement audio en Python
* [Augmentor](https://github.com/mdbloice/Augmentor) - Libraire d'augmentation d'imagerie en Python
* [PIL](https://www.pythonware.com/products/pil/) - Libraire de manipulation d'imagerie en Python
* [Starlette](https://www.starlette.io/) - Libraire de service ASGI en Python

### Outils de développement

* [Visual Studio Code](https://code.visualstudio.com/) - Éditeur de code
* [Android Studio](https://developer.android.com/studio) - Environnement de développement Android
* [Git](https://git-scm.com/) - Logiciel de gestion de versions décentralisé
* [Github](https://github.com/) - Service d'hébergement web pour Git
* [Google Colaboratory](https://colab.research.google.com/notebooks/welcome.ipynb) - Environnement de développement Jupyter en ligne avec un accès à des processeurs graphiques gratuit
* [Google One](https://one.google.com/) - Service de stockage nuagique
* [Clouderizer](https://clouderizer.com/) - Environnement de développement intégrer à Colab pour l'apprentissage machine
* [Trello](https://trello.com/) - Service web pour la création de liste sous forme de tableau Kanban

## Auteur

* Frédéric Larochelle - [Fredestroyer007](https://github.com/Fredestroyer007)

## Licence

Ce projet est distribué sous la licence GNU General Public License v3.0 - voir le fichier [LICENSE](LICENSE) pour plus de détails

## TODO 
Écran vue, diagramme
