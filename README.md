# pixijs-modules

## 1. getContentBoxSize.es6
这个模块用于获取带边框图形的原始尺寸，即不带边框时的尺寸。借用 css 中的概念不带边框叫 content-box。
调用方式：
1. 直接复制代码到项目中
2. `import ./path/getContentBoxSize.es6`
原谅我不会用 npm。

以下是一个 demo 代码：

```javascript
let polygon = new PIXI.Graphics(); 
polygon.beginFill(0xff0000)
    .lineStyle(20, 0xffff00, 1)
    .drawPolygon([0, 0, 0, 100, 80, 50])
    .closePath(); 
polygon.x = polygon.y = 100;  
stage.addChild(polygon); 
console.log("border-box:", polygon.width, polygon.height); // border-box: 95.29998940003179 116.95996608010176
console.log("content-box:", polygon.cwidth, polygon.cheight); // content-box: 80 100
```
