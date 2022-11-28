## A. COMMENT CONSTRUIRE

  ### Étape 1 : OBTENEZ LES OUTILS
 Installation de tous les outils nécessaires pour créer la page Web :

    
- [Git](https://git-scm.com/downloads) ; Nous avons utilisé git pour contrôler notre version dans gitlab
- [Github](https://about.gitlab.com/) ; Nous avons utilisé github comme serveur pour notre page Web
- [bureau Github] (https://www.gitbook.com/) ; Nous avons utilisé le bureau github pour transporter ou pousser notre codage de local à github
- [VScode](https://code.visualstudio.com/); Nous avons utilisé le code Visual Studio pour écrire nos documents
- [Nodejs](https://nodejs.org/en/); Nous l'avons utilisé pour construire l'environnement
- [Langage Markdown](https://www.nexmaker.com/doc/1projectmanage/markdown.html) ; Nous avons utilisé le langage Markdown pour écrire des documents

  ### Étape 2 : DÉFINIR LA PAGE
 Créez un référentiel : rendez-vous sur github.com et après vous être inscrit, créez votre référentiel. Gardez-le public afin que n'importe qui sur Internet puisse y avoir accès et ajoutez-y un fichier README car c'est là que vous pouvez écrire une longue description de votre projet.

<br>
<img style="float: center;" width=700 src="IMAGE/createrepository.png">


 REMARQUE : Ouvrez le référentiel, accédez aux paramètres, les pages sous la branche sélectionnez la source principale pour activer les pages Github pour ce référentiel et sous le dossier, sélectionnez racine et enregistrez (Attention ; vous avez sélectionné le dossier racine car vous n'avez pas encore installé de dossier docs pour ce référentiel , vous devrez donc modifier ce paramètre ultérieurement). Après avoir enregistré, vous obtiendrez le lien de votre référentiel.

<br>
<img style="float: center;" width=700 src="IMAGE/repositorylink.png">

  ### Étape 3 : PARAMÈTRES LOCAUX

   ### 1. Bureau Github

  Ouvrez le bureau Github, clonez votre référentiel créé précédemment et ouvrez-le dans Visual Studio Code.

<br>
<img style="float: center;" width=700 src="IMAGE/clone.png">



  ### 2. Code contre

  Dans VS Code, ajoutez le mot "Hello" au fichier README.md, enregistrez tout et utilisez le bureau github pour valider et pousser vers la page Web.
    Nous utilisons la méthode Docsify pour construire la structure, sous la barre de menu vscode ouvrez l'option Terminal et créez un nouveau terminal. Ensuite, installez doscsify.

<br>
<img style="float: center;" width=700 src="IMAGE/newterminal.png">


   ### 3. Install Docsify
 - Entrez d'abord la commande suivante "npm i docsify-cli -g"

<br>
<img style="float: center;" width=600 src="IMAGE/docsify.png">


  - Assurez-vous de la position puis initialisez l'environnement avec "docsify init ./docs"

  - Après une initialisation réussie, vous pouvez voir plusieurs fichiers créés dans le répertoire：
       index.html : fichier d'entrée.
    
       README.md : il sera rendu comme le contenu de la page d'accueil.
       .nojekyll : est utilisé pour empêcher les pages GitHub d'ignorer les fichiers commençant par un trait de soulignement.Aperçu
        
  - Entrez ce qui suit dans cmd.exe : docsify serve docs

  <br>
<img style="float: center;" width=600 src="IMAGE/doc2.png">


     
  - Ouvrez ensuite le navigateur pour visiter http://localhost:3000, vous obtiendrez un site Web initial.


   ### 4. Configurer Index.html

  <!DOCTYPE html>
     <html lang="en">
     <head>
         <meta charset="UTF-8">
         <title>test1page</title>
     </head>
     <body>
         <nav>
         <a href="https://www.nexmaker.com">nexmaker</a>
         <a href="https://fabacademy.org">fabacademy</a>
         <a href="bobwu0214@gmail.com">conact</a>
         </nav>
         <h1>hello world head1    </h1>
         <h2>hello world head2    </h2>
         <h3>hello world head1    </h3>
         <h4 align="center">hello world head2    </h4>
         <h4 style="background-color:red">This is a heading</h4>
         <b>This text is bold</b>
         <strong>This text is strong</strong>
         <p>paragraph1</p>
         <p>paragraph2</p>
         <hr />
         <p>paragraph3</p>
         <a href="www.nexmaker.com">This is a link</a>
         <img src="image/nexmakerlogo.jpg" width="160" height="160" />
         <hr/>
         <li><a href="http://ng.cba.mit.edu">A</a></li> 
         <li><a href="https://www.linkedin.com/in/saveriosilli">B</a></li> 
         <li><a href="https://www.linkedin.com/in/ted-hung-abbb806/">C</a></li> 
         <li><a href="https://www.linkedin.com/in/thunder-zhang-3b4090b">D</a></li> 
         <li><a href="xujunnature@gmail.com">E</a></li> 
     <!--mark,not show anything in web。-->
     </body>
     </html>

   ### 5. Ajouter une barre latérale et une barre de navigation
  - SIDEBAR 
              <!-- 侧边栏 docs/_sidebar.md -->
               - Team introduce
               - Daily homework
               - [1. PM]()
               - [how to build web](class/1pm/1pm-web.md)
               - introduce team
               - introduce finial project
               - [2. arduino basic]()
               - [3. CAD]()
               - [4. 3D printing]()
               - Final project
               - topic
               - innovation
               - market
               - how to design 
               - how to make
               - SDGs

 - ouvrez le fichier Index allez dans window.$docsify puis ajoutez

              loadSidebar: true,

 - Barre latérale pliable
pour rendre votre barre latérale pliable, il vous suffit d'ajouter ces éléments dans la fenêtre. $docsify this code


             subMaxLevel: 3,
             sidebarDisplayLevel: 1, // set sidebar display level

Insérez ensuite le script dans le document, tout comme l'utilisation des plugins officiels

              <!-- plugins -->
               <script src="//cdn.jsdelivr.net/npm/docsify-sidebar-collapse/dist/docsify-sidebar-collapse.min.js"></script>

- NAVBAR

Cree File Navbar.md

             <!-- 侧边栏 docs/_navbar.md -->
                - [VISION]()

                - [TEAM]()

                - [LANGUAGE]()

        - [:us:]()
        - [CN:cn:](CN/)
        - ع:saudi_arabia:

ouvre l'Index file va a window.$docsify puis ajoute

             loadNavbar: true,

 
   ### 6. Rédigez votre document et enregistrez tout le document.

   ### 7. Téléchargement d'images
 Nous avons créé un dossier Image dans docs où nous stockions toutes les images et nous les faisions glisser et déposer dans le document. en utilisant le format "img style="float: center;" width=700 src="IMAGE/Imageupload.png".

 <br>
<img style="float: center;" width=700 src="IMAGE/Imageupload.png">

 ### Étape 4 : TÉLÉCHARGER LE DOCUMENT
 1. Utilisez le bureau github pour télécharger de nouvelles informations en changeant le pli de la branche de root à docs.

<br>
<img style="float: center;" width=700 src="IMAGE/docs.png">


 2. Utilisez le bureau github pour nommer vos modifications et les valider. 

<br>
<img style="float: center;" width=700 src="IMAGE/changes.png">

3. Lorsque vous avez fini de les valider, vous pouvez pousser vos modifications sur votre page github.

<br>
<img style="float: center;" width=700 src="IMAGE/push.png">



## B. FAQ

 ## Choisir le dossier 'docs'
 Lors de la configuration de notre page, nous avions commencé par choisir le dossier "docs" plutôt que de choisir "root" qui, après l'enregistrement, ne nous donnait pas le lien de la page Web.

<br>
<img style="float: center;" width=700 src="IMAGE/repositorylink.png">

  ### SOLUTION : Nous avons découvert que nous devions choisir "root" en premier lieu car nous n'avions pas encore défini les paramètres locaux.

 ## Le terme 'npm' n'est pas reconnu comme le nom d'une applet de commande, d'une fonction, d'un fichier de script ou d'un programme utilisable
  programme utilisable était: npm i docsify-cli -g

   puis le système avertirait

   npm : le terme "npm" n'est pas reconnu comme le nom d'une applet de commande, d'une fonction, d'un fichier de script ou
   programme opérationnel. Vérifiez l'orthographe du nom, ou si un chemin a été inclus, vérifiez que
   le chemin est correct et réessayez.
   At line:1 char:2
   +  npm i docsify-cli -g
   +  ~~~
   + CategoryInfo          : ObjectNotFound: (npm:String) [], CommandNotFoundException        
   + FullyQualifiedErrorId : CommandNotFoundException

   <br>
   <img style="float: center;" width=700 src="IMAGE/owbsiqer.bmp">

     ### SOLUTION : Vérifiez le chemin ci-dessus

  ## Le terme 'docsify' n'est pas reconnu comme le nom d'une applet de commande, d'une fonction, d'un fichier de script ou d'un programme utilisable

  programme utilisable était : docsify init ./docs

  et le système avertirait

  <br>
 <img style="float: center;" width=700 src="IMAGE/docsify-prbjm.png">

    ### SOLUTION : Nous avons dû tout désinstaller et réinstaller car il s'agissait d'un problème d'environnement informatique.

  ## Échec du déploiement
  Parfois, nous poussions nos modifications sur la page et nous recevions une notification indiquant que le déploiement a échoué.

 <br>
 <img style="float: center;" width=700 src="IMAGE/deploy.png">

     ### SOLUTION : attendez un peu plus longtemps et réessayez, il s'agit principalement d'un problème de réseau.


## C. CONFIGURER TEAMINTRO

Obtenez un modèle que vous voudriez utiliser [Here](http://bestjquery.com/tutorial/our-team/demo65/)

<br>
<img style="float: center;" width=700 src="IMAGE/inspect.png">


<br>
<img style="float: center;" width=700 src="IMAGE/language2.png">


## D. LANGUAGE

normalement votre fichier docs ressemble à ceci

    .
    └── docs
       ├── README.md
       ├── index.htm
       ├── Sidebar.md
       └── navbar.md

si vous voulez avoir plus de langues, vous devez créer un autre dossier comme vous voulez faire du chinois afin que vous ayez un dossier comme la Chine de cette façon.

    .
    └── docs
       ├── README.md
       ├── Home.md
       ├── index.htm
       ├── Sidebar.md
       └── navbar.md
    └── China
       ├── Home.md
       ├── README.md
       ├── index.htm
       ├── Sidebar.md
       └── navbar.md
    └── French
       ├── Home.md
       ├── index.htm
       ├── Sidebar.md
       └── navbar.md
    └── README.md   

puis ajoutez dans le fichier d'index

     homepage: 'home.md',
     mergeNavbar: true,

<br>
<img style="float: center;" width=700 src="IMAGE/language.png">


## E. REFERENCES 
 - [Nexmaker](https://www.nexmaker.com/)
 - [Docsify](https://docsify.js.org/#/?id=docsify)
