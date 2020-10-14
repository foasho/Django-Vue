# Django-Vue.js

> Django+Vue Project

##環境構築

```commandline
npm install -g @vue/cli
vue init webpack .
>>AllEnter
npm run dev
>>確認
npm i bootstrap-vue --save
npm install sass-loader node-sass --save-dev

pip install django==2.2.0
django-admin startproject conf .
```

build/webpack.prod.jsの編集
```javascript
new CopyWebpackPlugin([
  {
    from: path.resolve(__dirname, '../src/assets'),
    to: config.build.assetsSubDirectory,
    ignore: ['.*']
  }
])
```

config/index.jsの編集
```javascript
build: {
    // Template for index.html
    index: path.resolve(__dirname, '../app/templates/index.html'),

    // Paths
    assetsRoot: path.resolve(__dirname, '../'),
    assetsSubDirectory: 'static',
    assetsPublicPath: '/',
    ・・・
}
```
