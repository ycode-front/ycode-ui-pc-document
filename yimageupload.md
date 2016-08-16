# 图片上传

##Example

```html
<!-- 图片上传组件 -->
    <div class="form-group">
        <label for="" class="control-label col-xs-4">图片上传</label>
        <div class="col-xs-5">
            <input type="text" class="form-control" id="upload-image" name="uploadit"/>
        </div>
    </div>
```

```javascript
/**
 * 图片上传组价
 */
// 初始化插件
$('#upload-image').yimageupload({
    url: 'image/save'
});

```

##Options

|name|type|required|default|description|
|:---|:---|:---:|:---||
|url|String|yes||必须设置，文件上传的url|
|fileNumber|numbrer|||最大文件的数量|
|fileNumberNow|number|||当前文件数量|
|widthLimit|number|||上传图片的宽度限制|
|heightLimit|number|||上传图片的高度限制|
|disabled|boolean||false||
|maxSize|||Infinity|设置文件最大大小|

##Events
|name|target|param|
|:---|:----|:---|
|imageupload.start|组件本身|无|
|imageupload.completed|组件本身|无|




