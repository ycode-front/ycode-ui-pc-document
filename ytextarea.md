# 多行文本
##Example

```html
<!-- 文本框 -->
    <div class="form-group">
        <label class="control-label col-xs-4">请输入你的理由</label>
        <div class="col-xs-5">
            <textarea class="form-control" id="js-textarea" rows="7" maxlength="100"></textarea>
        </div>
    </div>
```

```javascript

 /**
  *文本框
  */
$('#js-textarea').ytextarea({});

```
##Options
|name|type|required|default|description|
|:--|:--|:--|:--|:--|
|autosize|boolean|false|true|设置文本域是否会自动换行


