# 表单组件

## Example

```html
    <form class="js-form">
        <input type="text" name="text" value=""/>
    </form>
```

```javascript
    $('.js-form').yform({
        // 表单提交的目标
        action: '/apis/form-action.json',
        // 指定表单元素
        container: '.form-demo',
        // 表单的校验
        validate: {
            rules: {
                text: {
                    required: true
                }
            },
            messages: {
                text: {
                    required: '请输入理由'
                }
            }
        },
        // 表单提交按钮
        submitButton: '.js-submit',
        // 表单提交成功后调用
        success: function(res) {
            console.log(res);
            alert('提交成功');
        },
        // 挑担提交失败的时候调用
        error: function(res) {
            console.log(res);
            alert('提交失败')
        }
    })
```

## Options

|name|type|required|default|description|
|:---:|:---:|:---:|:---:|:---|
|action|string|true|''|表单提交的url|
|validate|object|false|{}|由于yform依赖jquery validation 插件，这个配置项也和 validate 配置项一致参考 [validate](https://jqueryvalidation.org/validate)|
|submitButton|string|false|''|提交按钮|
|direct|boolean|false|false|决定表单是否直接跳转提交或者发起异步请求提交|
|success|function|false|function(){}|回调函数，在表单提交成功之后调用|
|error|function|false|function() { Utils.alert("操作失败，请稍后再试或联系管理员"); }|回调函数，在表单提交失败之后调用|
|exception|function|false|function(){}|回调函数，在表单提交成功，但是 status 异常的情况下调用|
|submitByEnter|boolean|false|false|是否通过点击回车键进行提交|
|confirm|string|false|''|提交前的确认文案，如果不设置则不进行确认|
|errorPlacement|string|false|'inline'|(inline\|horizontal) 表单校验的错误提示位置是水平摆放还是换行|

## Methods

### .resetValidate()

重置校验提示，清空所有的校验错误提示

无参数

### .showError(name, errorMessage)

显示某一个字段的错误提示

参数

|name|type|required|default|description|
|:---|:---|:---:|:---||
|name|string|yes| |字段名|
|errorMessage|string|yes| |错误提示文案|

### .getData(callback)

获取表单中已经填写的数据，数据格式为序列化之后的数据

|name|type|required|default|description|
|:---|:---|:---:|:---||
|callback|function|yes| |回调函数用来接收表单数据|

### .valid()

手动触发表单的校验
