Using Fontawesome 5 with Laravel  
====

Font Awesome 5 を Laravel 5 で使う際に、手こずったので、備忘録

https://fontawesome.com/  

どうせなら、Font Awesome の SCSS版を使ってみる



## ■ npm 

```
npm install -g bower  
  --> %UserProfile%/AppData/Roaming/npm/node_modules/bower/bin/bower  
```



```
bower -v  
1.8.2
```



```
npm install -g gulp  
  --> %UserProfile%/AppData/Roaming/npm/node_modules/gulp/bin/gulp.js  
```



```
gulp -v  
3.9.1
```



```
npm install -g npm-check-updates
  --> %UserProfile%/AppData/Roaming/npm/node_modules/gulp/bin/gulp.js  
```



```
ncu -v  
2.14.0
```



## ■ fontawesome 

```
npm init
```



```
npm install axios cross-env bootstrap-sass jquery lodash vue laravel-mix  --save-dev --no-bin-links --no-optional  
```



```
npm install @fortawesome/fontawesome --save-dev --no-bin-links --no-optional  
npm install @fortawesome/fontawesome-free-brands --save-dev --no-bin-links --no-optional  
npm install @fortawesome/fontawesome-free-regular --save-dev --no-bin-links --no-optional  
npm install @fortawesome/fontawesome-free-solid --save-dev --no-bin-links --no-optional  
npm install @fortawesome/fontawesome-free-webfonts --save-dev --no-bin-links --no-optional  
```


## ■ Laravel 

scssファイルの編集 [./resources/assets/sass/app.scss]  
```
// Fontawesome 5  
@import "~@fortawesome/fontawesome-free-webfonts/scss/fontawesome";  
```


カスタムjsファイルの追加 [./resources/assets/js/fontawesome5.js]  
```
// fa本体  
const fontawesome = require("@fortawesome/fontawesome")  
// faライブラリ  
const faSolid = require("@fortawesome/fontawesome-free-solid")  
const faRegular = require("@fortawesome/fontawesome-free-regular")  
const faBrands = require("@fortawesome/fontawesome-free-brands")  
// faライブラリ登録  
fontawesome.library.add(faSolid, faRegular, faBrands)  
```

app.jsファイルの編集 [./resources/assets/js/app.js]  
```
require('./fontawesome5');  
```


## ■ npm run dev  

```
npm install -g cross-env  
npm run dev  
```



----------

php artisan serve  
http://localhost:8000/  

