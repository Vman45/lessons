# SPA - REACT 

## REACT:

1. [MVC](https://techaffinity.com/blog/mvc-architecture-benefits-of-mvc/)
2. [REACTJs](https://reactjs.org/)
3. [create-react-app](https://create-react-app.dev/)
4. [mainfest](https://web.dev/add-manifest/)

--------------------------------------------------------------------------------
5. create React App from scratch 
First step
```
$ npm init
```
then you need to install some packages 
```
$ npm i react
$ npm i react-dom
$ npm i react-scripts
$ npm i node-sass --save
```
for sure you need to create **.gitignore** and then create folders (src, public)
so your directory should look like
```
Project
│   README.md
│   package.json
|   package-lock.json
└───public
│   └───index.html
└───src
│   │   index.js
│   └───js
│   |   └───App.js
│   └───scss
        └───main.scss
   
```
Remember to add the important scripts to your __package.json__
```
  "scripts": {
    "start": "react-scripts start",
    "build": "react-scripts build"
  }
```




