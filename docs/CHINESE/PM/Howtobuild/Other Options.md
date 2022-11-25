# 1. LANGUAGE
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
    └── Arabic
     ├── Home.md
     ├── index.htm
     ├── Sidebar.md
     └── navbar.md
└── README.md   

then add in the index file

     homepage: 'home.md',
     mergeNavbar: true,

footer

footer: {
      copy: '<span>Acme &copy; 2022</span>',
      auth: 'by Mavericks',
      pre: '<hr/>',
      style: 'text-align: right;',
      class: 'className',
    },
<!-- add to to the end -->
    <script src="//unpkg.com/docsify-footer-enh/dist/docsify-footer-enh.min.js"></script>
Get a template you would want to use [Here](http://bestjquery.com/tutorial/our-team/demo65/)

