# 日期选择
##Example
```html
<!-- 日期选择框 -->
    <div class="form-group">
        <label class="control-label col-xs-4">出生日期</label>
        <div class="col-xs-2">
            <div class="input-group">
                <input class="form-control" id="date-picker" type="text"  placeholder="请选择日期" />
                <span class="input-group-addon">
                        <i class="fa fa-calendar bigger-110"></i>
                </span>
            </div>
        </div>
    </div>
```
```javascript
/**
 * 日期插件
 */
// 初始化插件
$('#date-picker').ydate({});
// 监听事件
$('#date-picker').on('input', function(){
    alert('input');
});
```
##options

|name|type|required|default|description|
|:---:|:---:|:---:|:---:|:---|
|unit|string|true|day|日期选择的单位day/month/year|
|startDate|string|false|''|起始日期|
|endDate|string|false|''|结束日期|

##Methods

###.getDate(date)
赶脚没用啊，呵呵哒。。。

###.setDate(date)
设置默认日期

###.setStartDate(startDate)
设置起始日期
参数

|name|type|required|default|descript|
|---|---|---|---|----|
|startDate|string|false|''|设置日期选择范围的起始日期，只有从该日期才可以被选择|

###.setEndDate(endDate)
设置日期选择范围的结束日期，请参考上面的setStartDate()


相关链接：[bootstrap-datepicker]( http://bootstrap-datepicker.readthedocs.io/en/latest/options.html )


