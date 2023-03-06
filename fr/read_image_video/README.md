## Lecture d'images et vidéos
![](https://img.shields.io/badge/lastest-2023--03--06-success)
![](https://img.shields.io/badge/status-en%20r%C3%A9daction%20-yellow)

Dans ce chapitre, On va parler de la façon de lire les images et les vidéos avec OpenCV. J'ai rassemblé un tas d'images et de vidéos que je vais utiliser chez moi. Tu devrais faire pareil de ton côté afin que tu puisses toi même tester les fonctions de traitement que je te montrerai à travers ce cour. Ce sont donc nos cobayes !<br/>



<details id="table-content" open>
    <summary>Table des Contenus</summary>
    <ul>
        <li><a href="#préparation">Préparation</a></li>
        <li><a href="#lecture-des-images">Lecture des images</a></li>
        <!-- <li><a href="#sous-linux">Sous Linux</a>
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
        </li> -->
    </ul>

</details>
<br/>

### Préparation
Dans un fichier python que tu vas créer et nommer `reader.py`, tu doit importer le module `cv2`, comme suit.

```python
import cv2 as cv

```

### Lecture des images
Pour lire des images dans openCV on utilise la fonction `imread()`. Elle prend un chemin vers une image et retorune cette image sous forme de matrice de pixels.

```python
# On lit l'images qui a pour nom de fichier `image01.jpg` qui se trouve
# dans le même répertoire que mon script `reader.py`.
image_matrix = cv.imread("images/image01.jpg")

# On lit l'image qui ce trouve dans mon répertoire `Pictures` de mon disque dur.
image_matrix = cv.imread("/home/dmk/Pictures/Screenshot_20230302_155530.png")

# Tu peux assi utiliser un chemin absolue vers l'image que tu veux lire.
```

Maintenant, une fois l'image lue, on peut l'afficher en utilisant la fonction `imshow()`. Cette fonction permet d'afficher l'image dans une nouvelle fenêtre. Les deux paramètres que nous devons renseigner à cette fonction sont en fait le nom de la fenêtre et la matrice de pixels à afficher, ici on va afficher l'image contenue dans la matrice `image_matrix`.

```python
# On passe le nom de la fênettre en premier et ensuite la variable contenant
# la matrice en second.
cv.imshow("My image", image_matrix)

# Tu dois ajouter la ligne de code supplémentaire.
cv.waitKey(0)

```

`waitKey()` est essentiellement une fonction de liaison au clavier, il attend un délai spécifique, ou un temps en millisecondes pour qu'une touche soit appuyée. Si tu lui passe `0`, il attend pendant un nombre de temps infini pour que la touche du clavier soit pressée.

Sauvegarde et exécute le script `reader.py` dans python. Et l'image s'affichera dans une fenêttre.

> Si la taille de l'image (largeur X hauteur) dépasse la taille de l'écran de ton ordinateur, tu ne verras qu'une partie de l'image s'afficher dans la fenêttre d'OpenCV.

<!-- 07:13 -->


<br/>
<br/>

<!-- - Je passe à la session **suivante**: [Installation et configuration](./installation/README.md) -->
[<--](./installation/README.md) Je reviens à la session **précédente**: [Installation et configuration](./installation/README.md)
