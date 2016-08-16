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
|url|String/Array|yes||表格的数据源,如果为 ``String`` 则判定为数据源的url，如果为 ``Array`` 则作为数据使用|
|fileNumber|numbrer|||最大文件的数量|
|fileNumberNow|number|||当前文件数量|
|labelLength|number||||
|widthLimit|number||||
|heightLimit|number||||
|disabled|boolean||false||



