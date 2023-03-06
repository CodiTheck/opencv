## Installation et configuration
![](https://img.shields.io/badge/lastest-2023--03--06-success)
<!-- ![](https://img.shields.io/badge/status-en%20r%C3%A9daction%20-yellow)-->

On aura besoin d'installater les outils de la liste ci-dessous:
- [python3](https://www.python.org/downloads/): L'interpretteur permettant d'exécuter du script Python.
- [python3-pip](https://www.google.com/search?q=python3-pip): Le scripte permettant d'installer les modules python. Je pense que ce scripte n'est utilisable que sous Linux. Les autres systèmes d'exploitation n'aurons pas bsoin de `python3-pip` mais d'un autre package permettant d'avoir `pip` pour installer des modules sur ton système. Tu peux utiliser [anaconda](https://anaconda.org/anaconda/python) comme alternative. Moi personnellement, je n'utilise pas `anaconda`.
- [python3-tk](https://www.google.com/search?q=python3-tk): Le programme est un utilitaire pour linux qui permet d'utiliser le module `tkinter` pour afficher les interfaces graphiques sous python. Il faut l'installer afin de pouvoir afficher les résultats produit par OpenCV dans une fenêttre.
- [virtualenv](https://virtualenv.pypa.io/en/latest/installation.html): Le sripte de gestion d'environnement virtuel pour python.
- [opencv-contrib-python](https://docs.opencv.org/4.x/): La bibliothèque de OpenCV qui contient toutes les fonctionnalités de vision par ordinateur. C'est elle qui fait l'objet de ce cour.

<details id="table-content" open>
    <summary>Table des Contenus</summary>
    <ul>
        <li><a href="#sous-windows-et-mac">Sous Windows et Mac</a></li>
        <li><a href="#sous-linux">Sous Linux</a>
            <ul>
                <li><a href="#installation">Installation</a>
                    <ul>
                        <li><a href="#installation-de-python">Installation de python</a></li>
                        <li><a href="#installation-de-virtualenv">Installation de virtualenv</a></li>
                        <li><a href="#installation-des-modules-fondamentaux">Installation des modules fondamentaux</a>
                            <ul>
                                <li><a href="#opencv">OpenCV</a></li>
                            </ul>
                        </li>
                    </ul>
                <li>
            </ul>
        </li>
    </ul>

</details>
<br/>

### Sous Windows et Mac
Je suis un peu désolé de te décevoir. Personnellement, je ne suis pas un grand fan des logiciels propriétaire. Donc, je n'ai pas l'habitude de travailler sur Windows et Mac. Pour cela, je te recommande d'aller suis des tutoriels sur comment installer les outils que je t'ai listé en haut.

### Sous Linux
> Dans ce cour et tous les autres cours à venir, si le symbole `~$` se trouve au début d'un block de code, cela signifie qu'il s'agit de lignes de commande qu'on peut exécuter dans un terminal.

#### Installation
##### Installation de python

```sh
# ~$
# Il faut copier et coller simplement le contenu de toute 
# cette case dans ton terminal et appuier sur la touche 
# [ENTER] de ton clavier.
sudo apt install python3;\
sudo apt install python3-pip python3-tk
```

Il faut s'assurer de la version de python qui est installée. La version de python
utilisée est `python 3.9.12`. Tu peux aussi utiliser la version `3.8`.

##### Installation de virtualenv
Il est fortement recommandé de travailler dans un environnement virtuel. Donc utilise une des commandes
suivant pour installer le gestionnaire d'environnement virtuel que je te propose.

```sh
# ~$
sudo apt install python3-venv
```

OU

```sh
# ~$
sudo pip3 install virtualenv
```

##### Installation des modules fondamentaux
Avant d'installer quoi que ce soit, il faut activer l'environnement virtuel. En fonction du choix 
d'installation du gestionnaire que tu a fait ci-dessus, exécute une des commandes suivante.

```sh
# ~$
# Si tu as installé le gestionnaire avec sudo apt install python3-venv,
# alors utilise ceci:
python3 -m venv env
```

OU

```sh
# ~$
# Si tu as installé le gestionnaire avec sudo pip3 install virtualenv,
# alors utilise ceci:
virtualenv env -p python3
```

###### OpenCV
Pour installer OpenCV, exécute la commande suivante dans ton environnement virtuel.

```sh
# ~$
pip install opencv-contrib-python
```

Certaines personnes te dirons d'installer juste le paquet `opencv-python`. Et bien, ce dernier est essentiellement le paquet principal de OpenCV. Ce pendant, `opencv-contrib-python` comprend non seullement le paquet principal, mais aussi des modules de contribution fournis par la communauté. Je te recommande donc de l'installer, car il contient toutes les fonctionnalités OpenCV.<br/>

Tu peux également remarquer que dans l'urgence,  le paquet `numpy` a été installé. Numpy est une bibliothèque de calcul scientifique en Python, qui est largement utilisé dans les manipulations de matrices, les transformations, le redimenssionnement et beaucoups d'autres opérations mathématiques. Nous allons utiliser `numpy` dans certaines parties de ce cours. Mais ne  t'inquiète pas si tu ne l'as jamais utilisé. C'est simple et relativement facile à utiliser.<br/>

Maintenant, le paquet suivant à installer est `caer`. Voici la commande:

```sh
# ~$
pip install caer
```

Je tiens à préciser qu'il s'agit d'un paquet que [jasmcaus](https://github.com/jasmcaus/caer) a créé pour accélérer le flux de travail. `caer` est essentiellement un ensemble de fonctions utilitaires qui seront très utiles dans ton parcours de vision par ordinateur. Il possède une tonne de fonctions d'aide super utiles qui t'aidera à accélérer ton flux de travail. Je ne vais tellement l'utiliser dans ce cour. Je vais plutôt l'utiliser dans les derniers chapitres. Je voulais jsute que tu l'installe maintenant afin de ne plus avoir à te soucier de son installation plus tard.<br/>

Dans le prochain chapitre, on verra comment lire des iamges et des vidéos avec OpenCV. Donc, on se revois au prochain chapitre.

<br/>
<br/>

- Je passe à la session **suivante**: [Lecture d'images et vidéos](../read_image_video/README.md)
- [<--](../README.md) Je reviens à la session **précédente**: [OpenCV](../README.md) -->

