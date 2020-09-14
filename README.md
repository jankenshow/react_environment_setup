# ra-men_app

### Environment
nodenv
node : v12.18.3  
npm : 6.14.8  
yarn : 1.22.5  

ES6+  
TypeScript  
React (Redux or Flux)  
Sass  
Babel  
Webpack  
Eslint  
Prettier  

### Directory structure

```
ra-menn_app
├── .babelrc
├── .eslintrc.js
├── .gitignore
├── .prettierrc
├── dist
│   └── bundle.js
├── package.json
├── postcss.config.js
├── src
│   ├── html
│   │   └── index.html
│   ├── index.tsx
│   └── scss
├── tsconfig.json
├── webpack.config.js
└── yarn.lock
```

JS files are transpiled to the directory as below.

entry : `src/index.tsx`  
output : `dist/bundle.js`  

And also HTML and CSS/SCSS under `src` directory are transpiled separately
into the `dist` directory.


### Installation

1. install nodenv
```
$ git clone git://github.com/nodenv/nodenv.git ~/.nodenv
$ echo 'export PATH="$HOME/.nodenv/bin:$PATH"' >> ~/.bashrc
$ echo 'if which nodenv > /dev/null; then eval "$(nodenv init -)" ; fi' >> ~/.bashrc
$ git clone https://github.com/nodenv/node-build.git ~/.nodenv/plugins/node-build
```

2. install node
```
$ . ~/.bash_rc
$ nodenv install v12.18.3
$ cd [where you create your app]
$ nodenv local v12.18.3
```

3. install packages
```
$ npm install -g yarn
$ . ~/.bash_rc
$ yarn install
```