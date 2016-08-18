# 下拉选择

##Example

```html
<!-- 下拉列表 -->
    <div class="form-group">
        <label class="control-label col-xs-4">出生年</label>
        <div class="col-xs-2">
            <select class="form-control" id="js-select" placeholder="请选择出生年月"></select>
        </div>
    </div>
```


```javascript

/**
 * 选择框
 */
$('#js-select')
    .yselect({
        dataSource:{
            url:'/apis/carport-status.json',
            params:{
                id:'hehe'
            }
        }
    })
    // 调用方法：设置参数
    .setParams({id:111})
    // 调用方法：更新数据
    .update();

```
## Options
|name|type|required|default|description|
|:---|:---|:---:|:---||
|dataSource|object/Array|yes||如果数据源为对象，则从接口获取数据，如果数据源是数组，则将数据源作为数据使用|
|dataSource.url|String|yes||下拉框的数据源url|
|dataSource.params|Object|no|{}|数据源的参数|

```javascript
/**
 * 选择框
 */
$('#js-select')
    .yselect({
        dataSource: [{
            "value": "1",
            "alias": "已购买1"
        }, {
            "value": "2",
            "alias": "已租用2"
        }, {
            "value": "3",
            "alias": "未使用3"
        }]
    })
    // 调用方法：设置参数
    .setParams({
        id: 111
    })
    // 调用方法：更新数据
    .update();

```

```javascript
/**
 * 选择框
 */
$('#js-select')
    .yselect({
        dataSource:{
            url:'/apis/carport-status.json',
            params:{
                id:'hehe'
            }
        }
    })
// 调用方法：设置参数
.setParams({id:111})
// 调用方法：更新数据
.update();

```


##Method

###setParams(params)
设置参数，使用对象扩展的方式
参数

|name|type|required|default|description|
|:---|:---|:---|:---|:---|
|params|object|false|{}|需要传递的参数json对象格式{key:value}|

###setDataSource(dataSource)
设置数据源

###update()
更新下拉数据

