Using Fontawesome 5 with Laravel  
====

Font Awesome 5 �� Laravel 5 �Ŏg���ۂɁA�肱�������̂ŁA���Y�^

https://fontawesome.com/  

�ǂ����Ȃ�AFont Awesome �� SCSS�ł��g���Ă݂�



## �� npm 

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



## �� fontawesome 

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


## �� Laravel 

scss�t�@�C���̕ҏW [./resources/assets/sass/app.scss]  
```
// Fontawesome 5  
@import "~@fortawesome/fontawesome-free-webfonts/scss/fontawesome";  
```


�J�X�^��js�t�@�C���̒ǉ� [./resources/assets/js/fontawesome5.js]  
```
// fa�{��  
const fontawesome = require("@fortawesome/fontawesome")  
// fa���C�u����  
const faSolid = require("@fortawesome/fontawesome-free-solid")  
const faRegular = require("@fortawesome/fontawesome-free-regular")  
const faBrands = require("@fortawesome/fontawesome-free-brands")  
// fa���C�u�����o�^  
fontawesome.library.add(faSolid, faRegular, faBrands)  
```

app.js�t�@�C���̕ҏW [./resources/assets/js/app.js]  
```
require('./fontawesome5');  
```


## �� npm run dev  

```
npm install -g cross-env  
npm run dev  
```



----------

php artisan serve  
http://localhost:8000/  

