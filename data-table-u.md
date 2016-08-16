# DataTable

## Example

```html
<table id="some-table" data-source="/apis/data.json"></table>
```

```json
{
    "status":0,
    "data":[{
        "orderId":1111111,
        "date":1231214124,
        "amount":1000.00
    },{
        "orderId":1111111,
        "date":1231214124,
        "amount":1000.00
    }]
}
```

```javascript
var dataTable = new DataTable({
    el:"#some-talbe",
    columns:[{
        alias: "订单编号",
        name: "orderId"
    },{
        alias: "数据量",
        name: "date"
    },{
        alias: "金额",
        name: "amount"
    }],
    operations:[{
        alias: "删除",
        todo: function(){
            alert('删除它！！！');
        }
    }]
});
```

## Options

|name|type|required|default|description|
|:---|:---|:---:|:---||
|dataSource|String/Array|yes||表格的数据源,如果为 ``String`` 则判定为数据源的url，如果为 ``Array`` 则作为数据使用|
|params|Object|no|{}|数据源的参数|
|paginable|Boolean|no|true|是否进行分页|
|batchable|Boolean|no|false|是否进行批量操作|
|columns|Array|no|[]|数据列配置|
|operations|Array|no|[]|数据列配置|

### columns item

|name|type|required|default|description|
|:---|:---|:---:|:---||
|alias|String|yes||显示的表格的title|
|name|String|yes||对应的属性名字|
|display|Function|no||对表格项的展示做重定义|

### operations item

|name|type|required|default|description|
|:---|:---|:---:|:---||
|alias|String|yes||显示操作的名字|
|className|String|no||操作的元素的类名，用来定义额外的样式|
|todo|Function|no||定义操作的行为, 回调函数中会传入，当前行的数据|
|show|Function|no||回调函数的结果作为示范显示的条件，回调返回true则显示，回调函数中会传入当前行的数据|


## Method

### refresh

刷新表格数据，一遍是在设置参数之后刷新数据

无参数

### setPage

设置分页

参数

|name|type|required|default|description|
|:---|:---|:---:|:---||
|pageObject|Object|yes| |分页信息|
|pageObject.page|Number|no| |页码|
|pageObject.size|Number|no| |每页信息量|

### extendParams

扩展请求数据的参数，之前设置的参数会被保留

参数

|name|type|required|default|description|
|:---|:---|:---:|:---||
|params|Object|yes| |数据请求的参数|

### replaceParams

替换请求数据的参数，之前设置的参数会丢失

参数

|name|type|required|default|description|
|:---|:---|:---:|:---||
|params|Object|yes| |数据请求的参数|

获取参数

## Property

### tableData

从接口中获取的表格数据

### params

通过 extendParams 和 replaceParams 所设置的值。

当没有任何设置的时候， params 默认为 {}

### page

用过 setPage 设置的分页信息

初始的时候是，``{page:1,size:10}``

会随着点击分页按钮而改变

### batchData

批量操作选中的数据，如果 ``batchable`` 选项为false，则 ``batchData`` 为``[]``

## Event

|name|target|param|condition|
|---|---|---|---|
|dataTable.updated|container||当每次数据刷新之后触发，包括第一次初始的时候刷新|
