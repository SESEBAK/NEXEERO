# 1. SET UP TEAMINTRO
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


# 2. LANGUAGE
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

