## A. HOW TO BUILD 

  ### Step 1: GET THE TOOLS
 Installing all the necessary tools to build the webpage:

    
- [Git](https://git-scm.com/downloads); We used git to control our version in gitlab
- [Github](https://about.gitlab.com/); We used github as a servicer for our webpage
- [Github desktop](https://www.gitbook.com/); We used github desktop to transport or push our coding from local to github
- [VScode](https://code.visualstudio.com/); We used the visual studio code to write down our documents
- [Nodejs](https://nodejs.org/en/); We used it to build the environment
- [Markdown language](https://www.nexmaker.com/doc/1projectmanage/markdown.html); We used the Markdown language to write documents

  ### Step 2: SET THE PAGE
 Create a repository: go on github.com and after signing up, create your repository. Keep it Public so that anyone on the internet can have access to it and add a README file to it cause that's where you can write a long description for your project. 

<br>
<img style="float: center;" width=700 src="IMAGE/createrepository.png">


 NOTE: Open the repository go to settings, pages under branch select the main source to enable Github pages for this repository and under folder select root and save(Attention; you selected root folder because you havn't yet installed a docs folder for this repository, therefore you will have to change this setting later). After saving you will get your repository link.

<br>
<img style="float: center;" width=700 src="IMAGE/repositorylink.png">

  ### Step 3: LOCAL SETTINGS

   ### 1. Github Desktop

  Open Github desktop, clone your repository created earlier on and open it in Visual Studio Code.

<br>
<img style="float: center;" width=700 src="IMAGE/clone.png">



   ### 2. Vs Code

  In VS Code, Add "Hello" word to the README.md save all and use github desktop to commit and push to the web page.
    We use the Docsify methode to build the structure, under the vscode menu bar open the Terminal option and create a new terminal. Then install doscsify.

<br>
<img style="float: center;" width=700 src="IMAGE/newterminal.png">


   ### 3. Install Docsify
  -  Enter the following command first "npm i docsify-cli -g"

<br>
<img style="float: center;" width=600 src="IMAGE/docsify.png">


  -  Make sure the position and then initialize environment with "docsify init ./docs"

  - After successful initialization, you can see several files created in the directory：
       index.html: Entry File.
    
       README.md: It will be rendered as the homepage content.
       .nojekyll: Is Used to prevent GitHub Pages from ignoring files that begin with an underscore.Preview
        
  - Enter the following in cmd.exe: docsify serve docs

  <br>
<img style="float: center;" width=600 src="IMAGE/doc2.png">


     
  - Then open browser to visit http://localhost:3000, you will get a initial website.


   ### 4. Setting up Index.html

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

   ### 5.  Add sidebar and navbar
  - SIDEBAR 
              - DAILY HOMEWORL
             - [1. HOW TO BUILD WEB]()
             -  2. CAD DESIGN
                - [Fusion 360]()
                - [Practices]()
             -  3. 3D PRINTING
                - [Theory]()
                - [Practice]()
                - [Postprocessing]()
             -  4. LASER CUTTING
                - [Basics]()
                - [Practice]()
            -  5. ARDUINO
                - [Theory]()
                - [Practice]()
            -  6. PROGRAMMING 
                - [Theory]()
                - [Practice]()

             - FINAL PROJECT
                - [SDG]()
                - [Topic]()
                - [User Research]()
                - [Market]()
                - [Innovation]()
                - [Key Technology]()
                - [How To Make]()

      - open the Index file go to window.$docsify then add

              loadSidebar: true,

 - collapsible Sidebar
to make your sidebar collapsible you just need to these things add in window.$docsify this code


             subMaxLevel: 3,
             sidebarDisplayLevel: 1, // set sidebar display level

Then insert script into document just like the official plugins's usage

              <!-- plugins -->
               <script src="//cdn.jsdelivr.net/npm/docsify-sidebar-collapse/dist/docsify-sidebar-collapse.min.js"></script>

- NAVBAR

Creat File Navbar.md

             - [VISION](INTRO/NAVBAR/Vision.md)



             - [TEAM](INTRO/NAVBAR/Team.md)



             - LANGUAGE
              - [FRENCH](/FRENCH/)
              - [CHINESE](/CHINESE/)

open the Index file go to window.$docsify then add

             loadNavbar: true,

 
   ### 6. Write your document and save all the document.

   ### 7. Image Upload
 We created an Image folder in docs where we stored all the pictures and we would drag and drop them into the document. using "img style="float: center;" width=700 src="IMAGE/Imageupload.png" format.

 <br>
<img style="float: center;" width=700 src="IMAGE/Imageupload.png">

 ### Step 4: UPLOAD DOCUMENT
 1. Use github desktop to upload new information by changing the branch's fold from root to docs.

<br>
<img style="float: center;" width=700 src="IMAGE/docs.png">


 2. Use github desktop to name your changes and to commit them. 

<br>
<img style="float: center;" width=700 src="IMAGE/changes.png">

 3. when you are done committing them, you can push your changes to your github page.

<br>
<img style="float: center;" width=700 src="IMAGE/push.png">



## B. FAQ

 ## Choosing 'docs' folder 
 When setting up our page we had started by choosing the folder "docs" rather that choosing "root" which after saving was not giving us the webpage link.

<br>
<img style="float: center;" width=700 src="IMAGE/repositorylink.png">

   ### SOLUTION: We discovered that we had to choose "root" in the first place because we had not yet put the local settings.

 ## The term 'npm' is not recognized as the name of a cmdlet, function, script file, or operable  program
  operable program was:     npm i docsify-cli -g

   and then system would warn

   npm : The term 'npm' is not recognized as the name of a cmdlet, function, script file, or 
   operable program. Check the spelling of the name, or if a path was included, verify that 
   the path is correct and try again.
   At line:1 char:2
   +  npm i docsify-cli -g
   +  ~~~
   + CategoryInfo          : ObjectNotFound: (npm:String) [], CommandNotFoundException        
   + FullyQualifiedErrorId : CommandNotFoundException

   <br>
   <img style="float: center;" width=700 src="IMAGE/owbsiqer.bmp">

     ### SOLUTION: Verify the path above

  ## The term 'docsify' is not recognized as the name of a cmdlet, function, script file, or operable  program

  operable program was:    docsify init ./docs

  and the system would warn

  <br>
 <img style="float: center;" width=700 src="IMAGE/docsify-prbjm.png">

     ### SOLUTION: We had to disinstall and re-install everything as it was a computer environment issue.

  ## Failed to Deploy
  Sometimes we would push our changes to the page and we would have a notification that deployment has failed. 

 <br>
 <img style="float: center;" width=700 src="IMAGE/deploy.png">

     ### SOLUTION: Wait a bit longer and keep trying again, it is mainly a network issue.


## C. SET UP TEAMINTRO

Get a template you would want to use [Here](http://bestjquery.com/tutorial/our-team/demo65/)

<br>
<img style="float: center;" width=700 src="IMAGE/inspect.png">


<br>
<img style="float: center;" width=700 src="IMAGE/language2.png">

       <div class="demo">
       <div class="container">
       <div class="row text-center">
       <h1 class="white" style="text-align:center; font-size:40px;">MEET THE TEAM</h1>
       </div>

       <div class="row">
       <div class="col-md-4 col-sm-6">
       <div class="our-team">
       <div class="pic">
       <img src="IMAGE/rema.jpg" alt=""/>
       </div>
       <div class="team-content">
       <h3 class="title">Raoul REMA</h3>
       <span class="post">Project Developper</span>
       <p class="description" style="text-align:justify;">
                                
                            </p>
                        </div>
                    </div>
                </div>

       <div class="col-md-4 col-sm-6">
                    <div class="our-team">
                        <div class="pic">
                            <img src="IMAGE/serena.jpg" alt=""/>
                        </div>
                        <div class="team-content">
                            <h3 class="title">Serena BAKANIBONA</h3>
                            <span class="post">Web Designer</span>
                            <p class="description">
                                
                            </p>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>
      <div class="demo">
        <div class="container">
            

          <div class="row">
                <div class="col-md-4 col-sm-6">
                    <div class="our-team">
                        <div class="pic">
                            <img src="IMAGE/lerato.JPG" alt=""/>
                        </div>
                        <div class="team-content">
                            <h3 class="title">Lerato LESAOANA</h3>
                            <span class="post"> Team Researcher</span>
                            <p class="description">
                                  
                        </div>
                    </div>
                </div>

          <div class="col-md-4 col-sm-6">
                    <div class="our-team">
                        <div class="pic">
                            <img src="IMAGE/hamzah.JPG" alt=""/>
                        </div>
                        <div class="team-content">
                            <h3 class="title">Hamzah ALKUREIBY</h3>
                            <span class="post">Team Researcher</span>
                            <p class="description">
                           
                            </p>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>



## D. LANGUAGE

normaly your docs file look like this

    .
    └── docs
       ├── README.md
       ├── index.htm
       ├── Sidebar.md
       └── navbar.md

if you want to have more languages you need creat another follder like you want make chinese so you haave have follder like China like this way.

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

then add in the index file

     homepage: 'home.md',
     mergeNavbar: true,

<br>
<img style="float: center;" width=700 src="IMAGE/language.png">


## E. REFERENCES 
 - [Nexmaker](https://www.nexmaker.com/)
 - [Docsify](https://docsify.js.org/#/?id=docsify)
