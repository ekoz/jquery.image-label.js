## jquery.image-label.js
    图片标签插件，用于描述图片中的特征事物，主要应用场景是图像识别后的特征展示。

### 依赖
该插件依赖于 [jquery](http://jquery.com/)

### 用法
```
//初始化
$('img').imageLabel();
//加载数据
var _arr = JSON.parse(localStorage.getItem('labelArr')); //[{"text":"主队","index":"1","top":"139","left":"778"},{"text":"客队","index":"2","top":"98","left":"483"}]
$('img').imageLabel('loadData', {
    data: _arr
});
//create
$('#btnCreate').click(function(){
    //$('img').imageLabel('create');
    $('img').imageLabel('create', {
        text: '勒布朗詹姆士'
    });
});
//save
$('#btnSave').click(function(){
    var data = $('img').imageLabel('getData');
    localStorage.setItem('labelArr', JSON.stringify(data));
});
```
### Demo
[单击这里](demo/demo.html)
![demo](demo/demo.gif)
