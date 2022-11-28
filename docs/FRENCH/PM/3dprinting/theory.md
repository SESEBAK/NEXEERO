<br>
 <img style="float: center;" width=700 src="IMAGE/3d.png">

# Première étape – Création
Tout d'abord dans l'impression 3D consiste à créer un fichier numérique en trois dimensions de l'objet que nous voulons imprimer. La manière la plus courante de créer un modèle numérique est la conception assistée par ordinateur - CAO. Cependant, il existe une large gamme de logiciels professionnels et d'entrée de gamme qui peuvent produire un fichier adapté à l'impression 3D.

- DESIGN : vous pouvez utiliser un logiciel de modélisation 3D comme Blender, SketchUp, AutoCad, SolidWorks, Maya, PhotoShop, ThinkerCad ou d'autres pour créer vos propres conceptions. Nous avons utilisé Fusion360 pour toutes les conceptions de ce projet.
- SCAN : une autre façon de créer un fichier numérique en trois dimensions consiste à numériser en 3D. La numérisation 3D est une technologie étroitement liée à l'impression 3D, qui analyse un objet du monde réel et crée instantanément une réplique numérique. La numérisation 3D est largement utilisée pour les tâches de rétro-ingénierie par les professionnels de l'industrie. Une fois qu'un objet existant est numérisé, nous avons également la possibilité de le modifier avant l'impression. Un scanner 3D est nécessaire pour ce processus.
- TÉLÉCHARGER : si vous avez un minimum de patience et que vous voulez simplement imprimer quelque chose, vous pouvez visiter des sites Web comme Thingivers, YouMagine, CrabCad et MyMinifactory Shapeways pour télécharger ou acheter des fichiers que d'autres utilisateurs ont modélisés. Ces fichiers sont prêts pour l'impression 3d dans la plupart des cas !

Enfin, les fichiers 3D doivent répondre à plusieurs exigences de conception avant de les envoyer à l'imprimante. Lors de la conception pour la fabrication additive (impression 3D), nous devons garder à l'esprit que nous concevons pour le monde réel. Ce sont des choses comme la bonne taille d'échelle, l'épaisseur de paroi minimale, le collecteur / étanche pour n'en nommer que quelques-uns, que nous allons approfondir un peu plus tard.

[Liens vers des logiciels de conception gratuits, des fichiers prêts à imprimer et des moteurs de découpage](http://my3dconcepts.com/explore/design-scan-download/)


# Deuxième étape - STL
Une fois que vous avez terminé la conception CAO, il est temps de l'envoyer à l'imprimeur. Tout d'abord, nous devons le convertir dans un format de fichier approprié. Le format de fichier d'impression 3D le plus courant est appelé STL, qui signifie STereoLithography, et nommé d'après le tout premier processus d'impression 3D. STL a plusieurs autres significations telles que "Standard Triangle Language" et "Standard Tessellation Language". Ce qu'il est important de retenir ici, c'est que .STL est l'extension de fichier utilisable.

Ce format de fichier comprend un maillage triangulaire (polygones), les données qui décrivent la disposition/surface d'un objet tridimensionnel. Les alternatives à STL sont .OBJ et .3MF. Gardez à l'esprit que tous ces formats de fichiers ne contiennent pas d'informations sur les couleurs. Pour l'impression 3D en couleur, vous devez utiliser des formats de fichiers tels que .X3D, .WRL, .DAE, .PLY

Une remarque importante ici n'est pas que tous les fichiers STL ou OBJ sont imprimables en 3D par défaut. Les formats de fichiers doivent répondre à certains critères tels qu'un nombre maximal de polygones, une étanchéité à l'eau, une taille physique appropriée, une épaisseur de paroi minimale, etc. (Lire la suite ici.) En bref, ils doivent être conçus en pensant à l'impression 3D !
Tranchage – FAO

<br>
 <img style="float: center;" width=700 src="IMAGE/stl.png">

# Troisième étape - Trancher
Il s'agit du processus de traduction du fichier 3D en instructions à suivre par l'imprimante 3D. Oui, c'est la partie amusante et vous avez besoin d'un logiciel spécial pour ne faire que cela ! Fondamentalement, Slicing divise ou découpe le modèle 3D en centaines ou milliers de couches horizontales, indiquant à la machine exactement quoi faire, étape par étape.

Le logiciel utilisé est [Flashforge 3D Printer](https://www.flashforge.com/download-center)

<br>
 <img style="float: center;" width=700 src="IMAGE/slice.png">


Une fois les fichiers découpés en tranches, un nouveau format de fichier est généré, appelé G-code, avec l'extension de fichier .gcode. Le G-code est le langage de programmation de code numérique le plus largement utilisé, principalement utilisé dans la fabrication assistée par ordinateur pour contrôler les machines-outils automatisées telles que les imprimantes 3D et les CNC (commandes numériques par ordinateur). En un mot, le G-code est le langage de la machine et ce que nous utilisons pour communiquer avec elle !

Si vous possédez une imprimante 3D, vous devrez le faire vous-même. Il existe de nombreux paramètres que vous pouvez ajuster pour obtenir le meilleur résultat de l'imprimante. La bonne nouvelle est qu'aucun codage n'est requis du tout 😉

Si vous utilisez un fournisseur de services d'impression 3D, vous n'avez pas à vous soucier du découpage. Pourquoi? Parce que le fournisseur le fera pour vous. Tout ce que vous avez à faire est de télécharger le bon format de fichier et d'attendre la fin du processus d'impression 3D.

<br>
 <img style="float: center;" width=700 src="IMAGE/send.png">

# Step Four – Printing

<br>
 <img style="float: center;" width=400 src="IMAGE/1step.jpg">

<br>
 <img style="float: center;" width=400 src="IMAGE/levels.jpg">

<br>
 <img style="float: center;" width=400 src="IMAGE/4step.png">

<br>
 <img style="float: center;" width=400 src="IMAGE/5step.png">


Les machines d'impression sont constituées de nombreuses pièces mobiles et complexes, et elles nécessitent un entretien et un étalonnage corrects pour produire des impressions réussies. La plupart des imprimantes 3D n'ont pas besoin d'être surveillées après le début de l'impression. La machine suivra les instructions automatisées du code G, donc tant qu'il n'y a pas d'erreur logicielle ou que la machine ne manque pas de matière première, il ne devrait pas y avoir de problèmes pendant le processus d'impression.

# Cinquième étape - Suppression
Le retrait des pièces finies de l'imprimante varie selon les différentes technologies d'impression 3D. Dans certains cas, comme pour les ordinateurs de bureau, il suffit de séparer l'impression de la plate-forme de construction. Pour certaines imprimantes 3D industrielles, le retrait d'une pièce est un processus technique qui nécessite des compétences professionnelles et des équipements spécialisés dans un environnement contrôlé.

<br>
 <img style="float: center;" width=400 src="IMAGE/postp.png">


# REFERENCES
1. [Nexmaker](https://www.nexmaker.com/doc/3_3dprinter/1.3Dprintingbackground.html)
2. [3D CONCEPTS](http://my3dconcepts.com/explore/how-3d-printing-works/)