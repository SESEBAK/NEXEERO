## A. 如何构建

  ### 第 1 步：获取工具
 安装构建网页所需的所有工具：

    
- [Git](https://git-scm.com/downloads);我们在gitlab中使用git来控制我们的版本
- [Github](https://about.gitlab.com/)；我们使用 github 作为我们网页的服务商
- [Github桌面](https://www.gitbook.com/)；我们使用 github desktop 将我们的代码从本地传输或推送到 github
- [VScode](https://code.visualstudio.com/);我们使用 visual studio code 来写下我们的文档
- [Nodejs](https://nodejs.org/en/);我们用它来搭建环境
- [Markdown 语言](https://www.nexmaker.com/doc/1projectmanage/markdown.html)；我们使用 Markdown 语言编写文档

  ### 第 2 步：设置页面
 创建存储库：访问 github.com 并在注册后创建您的存储库。保持公开，以便互联网上的任何人都可以访问它并向其中添加一个 README 文件，因为这是您可以为您的项目编写详细描述的地方。 

<br>
<img style="float: center;" width=700 src="IMAGE/createrepository.png">


 注意：打开存储库转到设置，分支下的页面选择主要来源以为此存储库启用 Github 页面，并在文件夹下选择根目录并保存（注意；您选择根文件夹是因为您尚未为此存储库安装文档文件夹，因此您稍后必须更改此设置）。保存后，您将获得存储库链接。

<br>
<img style="float: center;" width=700 src="IMAGE/repositorylink.png">

  ### 第 3 步：本地设置

   ### 1. Github桌面

  打开 Github 桌面，克隆之前创建的存储库并在 Visual Studio Code 中打开它。

<br>
<img style="float: center;" width=700 src="IMAGE/clone.png">



   ### 2. 对比代码

  在 VS Code 中，在 README.md 中添加“Hello”字样，全部保存并使用 github desktop 提交并推送到网页。
    我们使用Docsify方法搭建结构，在vscode菜单栏下打开Terminal选项，新建一个终端。然后安装 doscsify。

<br>
<img style="float: center;" width=700 src="IMAGE/newterminal.png">


   ### 3. 安装 Docsify
  - 先输入以下命令“npm i docsify-cli -g”

<br>
<img style="float: center;" width=600 src="IMAGE/docsify.png">


  - 确保位置，然后使用“docsify init ./docs”初始化环境

  - 初始化成功后，可以看到目录下创建了几个文件：
       index.html：入口文件。
    
       README.md：它将被渲染为首页内容。
       .nojekyll：用于防止 GitHub Pages 忽略以下划线开头的文件。预览
        
  - 在 cmd.exe 中输入以下内容：docsify serve docs

  <br>
<img style="float: center;" width=600 src="IMAGE/doc2.png">


     
  - 然后打开浏览器访问http://localhost:3000，你会得到一个初始网站。


   ### 4. 设置 Index.html
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

 ### 5.添加侧边栏和导航栏
  - SIDEBAR 
              <!-- 侧边栏 docs/_sidebar.md -->
               - 日常作业
             - [1。如何建立网站]()
             - 2。 CAD 设计
                 - [Fusion 360]()
                 - [练习]()
             - 3。 3D 打印
                 - [理论]()
                 - [练习]()
                 - [后期处理]()
             - 4。激光切割
                 - [基础知识]()
                 - [实践]()
             - 5。阿杜诺
                 - [理论]()
                 - [练习]()
             - 6. 编程
                 - [理论]()
                 - [练习]()

               - 最终项目
             - [SDG]()
             - [话题]()
             - [用户研究]()
             - [市场]()
             - [创新]()
             - [关键技术]()
             - [怎么做]()

 - open the Index file go to window.$docsify then add

              loadSidebar: true,

 - 可折叠的侧边栏
要使侧边栏可折叠，您只需要将这些东西添加到 window.$docsify 这段代码中


             subMaxLevel: 3,
             sidebarDisplayLevel: 1, // set sidebar display level

然后像官方插件的用法一样将脚本插入到文档中

              <!-- plugins -->
               <script src="//cdn.jsdelivr.net/npm/docsify-sidebar-collapse/dist/docsify-sidebar-collapse.min.js"></script>

- NAVBAR

创建文件 Navbar.md

             - [想象]()



             - [团队]()


             - [语]
                - [英语]()
                - [法语]()


打开索引文件转到 window.$docsify 然后添加

             loadNavbar: true,

 
   ### 6. 编写文档并保存所有文档。

   ### 7. 图片上传
 我们在 docs 中创建了一个 Image 文件夹，我们在其中存储了所有图片，我们会将它们拖放到文档中。使用 "img style="float: center;" width=700 src="IMAGE/Imageupload.png" 格式.

 <br>
<img style="float: center;" width=700 src="IMAGE/Imageupload.png">

 ### 第 4 步：上传文件
 1.使用github desktop通过将分支的fold从root更改为docs来上传新信息。

<br>
<img style="float: center;" width=700 src="IMAGE/docs.png">


 2. 使用 github desktop 命名您的更改并提交它们。 

<br>
<img style="float: center;" width=700 src="IMAGE/changes.png">

 3. 完成提交后，您可以将更改推送到您的 github 页面。

<br>
<img style="float: center;" width=700 src="IMAGE/push.png">



## B.常见问题解答

 ## 选择“文档”文件夹
 在设置我们的页面时，我们首先选择文件夹“docs”而不是选择“root”，这在保存后并没有给我们网页链接。

<br>
<img style="float: center;" width=700 src="IMAGE/repositorylink.png">

   ### 解决方案：我们发现我们必须首先选择“root”，因为我们还没有进行本地设置。

 ## 术语“npm”未被识别为 cmdlet、函数、脚本文件或可运行程序的名称
  可运行的程序是：npm i docsify-cli -g

   然后系统会警告

   npm：术语“npm”未被识别为 cmdlet、函数、脚本文件或
   可运行的程序。检查名称的拼写，或者如果包含路径，请验证
   路径正确，然后重试。
   At line:1 char:2
   +  npm i docsify-cli -g
   +  ~~~
   + CategoryInfo          : ObjectNotFound: (npm:String) [], CommandNotFoundException        
   + FullyQualifiedErrorId : CommandNotFoundException

   <br>
   <img style="float: center;" width=700 src="IMAGE/owbsiqer.bmp">

    ### 解决方案：验证上面的路径

  ## 术语“docsify”未被识别为 cmdlet、函数、脚本文件或可运行程序的名称

  可运行的程序是：docsify init ./docs

  并且系统会警告

  <br>
 <img style="float: center;" width=700 src="IMAGE/docsify-prbjm.png">

     ### 解决方案：我们不得不卸载并重新安装所有内容，因为这是计算机环境问题。

  ## 部署失败
  有时我们会将更改推送到页面，并且会收到部署失败的通知。

 <br>
 <img style="float: center;" width=700 src="IMAGE/deploy.png">

     ### 解决方法：稍等片刻再试，主要是网络问题。


## C. 设置 TEAMINTRO

获取您想要使用的模板 [Here](http://bestjquery.com/tutorial/our-team/demo65/)

<br>
<img style="float: center;" width=700 src="IMAGE/inspect.png">


<br>
<img style="float: center;" width=700 src="IMAGE/language2.png">


## D. 语言

通常你的文档文件看起来像这样

    .
    └── docs
       ├── README.md
       ├── index.htm
       ├── Sidebar.md
       └── navbar.md

如果你想要更多的语言，你需要创建另一个文件夹，就像你想要制作中文一样，这样你就可以像这样拥有像中国这样的文件夹。

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

然后在索引文件中添加

     homepage: 'home.md',
     mergeNavbar: true,

<br>
<img style="float: center;" width=700 src="IMAGE/language.png">


## E. 参考文献 
 - [Nexmaker](https://www.nexmaker.com/)
 - [Docsify](https://docsify.js.org/#/?id=docsify)
