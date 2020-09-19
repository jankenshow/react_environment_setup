# For react app environment setup

### Environment
node (nodenv) : v12.18.3  
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
app
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

3. Change app name  
at package.json  
```{json:package.json}
{
  "name": "app",　# ← anything you like
  "version": "1.0.0",
  ・・・
```

4. install packages
```
$ npm install -g yarn
$ . ~/.bash_rc
$ yarn install
```

5. run dev-server
```
$ yarn start
```

6. browse your app  
visit http://localhost:8080 on browser  

if you would like to change port number, edit webpack.config.js #L23  
https://github.com/jankenshow/react_environment_setup/blob/master/webpack.config.js#L23
```{js:webpack.config.js}
・・・
    devServer: {
        contentBase: dist,
        port: 8080, # ← here
        open: false,
        historyApiFallback: true,
        inline: true,
        hot: true
    },
・・・
```
