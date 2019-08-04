# RxJs - Reactive X - [javascript]

1- create folder rxjs-basic
2- npm init
3- npm install rxjs --save
4- npm install webpack-dev-server typescript typings ts-loader --save-dev
5- npm install webpack
5- npm install webpack-cli


      (To use latest features of Javascript ECMA 2015 sepcifications aka ES6, We need compiler or transpiler that takes javascript code and transpiles in ES5, and we also need module bundler which takes the code along with rxjs code and generates 1 file to serve to browser)
 web-dev-server (development web server)
 typescript/babel (babel if you write in plain javascript)
 ts-loader (tool that helps to work with typescript)


We need to setup Type Definition (Where typescript can understand all capabilities of RxJs)
Since Rxjs is developed with ES6 in mind, Then RxJs uses features and API that are native to ES6 like (map, set datastructures) and new methods on array and string. Typescript has no information for this, We can bridge this.

Goto node_modules directory and .bin
node_modules/.bin/typings  install dt~es6-shim --global


236 Votes :
You should change loaders to rules in webpack 4:
change:
      loaders 
      to:
      rules


If you are using rxjs >=6.0.0 then you no longer use Observable.from. Instead from is a standalone function.

import { Observable, from} from 'rxjs';

//old way
var o = Observable.from([1, 2, 3, 4]);

//new way
var o = from([1, 2, 3, 4]);
