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
|dataSource|String/Array|yes||下拉框的数据源,如果为 ``String`` 则判定为数据源的url，如果为 ``Array`` 则作为数据使用|
|params|Object|no|{}|数据源的参数|

##Method

###setParams
设置参数，使用对象扩展的方式

###setDataSource
设置数据源

###update
更新数据

