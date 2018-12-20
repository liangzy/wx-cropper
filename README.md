### 更新日志
- 编写2.0版本，添加裁剪区域宽度高度比例的控制，而不是以往的750 * 750 而导致页面显示的内容不充分的视觉效果（通过 CROPPER_RATIO 来控制cropper的宽高比例  默认是0.6666 接近于宽640 / 高960）
- 添加固定比例裁剪功能 CROPPER_AREA_RATIO 在设置为 > 0 的number值的时候可以控制裁剪的比例，比例也是宽高的比，如果是正方形则为1，如果不想有比例的裁剪，这个常量设置为0 即可
- 优化界面UI
- 这些代码还有部分问题，暂时没有放到master，有需要或者了解的可在v2分支拉取代码

# wx-cropper
微信小程序  图片裁剪工具，简单易用

QQ交流群： 424418160

### 项目需求
在做微信小程序的时候有个图片上传之前裁剪的需求，找过一些github中的项目，都不太理想，主要是没有办法自定义宽高，于是自己研究了一下，做了一个简单的图片裁剪效果

### 使用方法
项目里面直接放的该功能的文件，将这个文件夹复制到小程序项目中，在app.json中启动该页面即可看到效果


### 注意：这里面的图片在你们的项目中可能会无法使用，在测试的话 可以用自己本地或者你们项目服务器下的图片地址

### 显示效果
![](https://github.com/IFmiss/wx-cropper/blob/v2/1.png) 
这是在裁剪区域设定不设置固定裁剪框的宽高比例，加载的时候会覆盖整张图片
```js
CROPPER_AREA_RATIO = 0
```

![](https://github.com/IFmiss/wx-cropper/blob/v2/2.png) 
裁剪区域固定宽高
```js
CROPPER_AREA_RATIO = 0
```

#### 裁剪之后的效果
![](https://github.com/IFmiss/wx-cropper/blob/v2/3.png) 