# 日期范围选择

##Example

```html
<!-- 日期范围选择框 -->
<div class="form-group">
    <label class="control-label col-xs-4">日期范围</label>
    <div class="col-xs-3">
        <div class="input-group input-daterange" id="js-daterage">
            <input type="text" class="form-control" name="start" placeholder="起始日期" value="2016-01"/>
            <span class="input-group-addon">
                <i class="fa fa-exchange"></i>
            </span>
            <input type="text" class="form-control" name="end"  placeholder="结束日期" value="2016-02">
        </div>
    </div>
</div>
```

```javascript
    $('#js-daterage').ydaterange({
            unit: 'year',
            startDate: '2010',
            endDate: '2020'
        });
```

##Options

|name|type|required|default|description|
|:---:|:---:|:---:|:---:|:---|
|unit|string|true|day|日期选择的单位day/month/year|
|startDate|string/object|false|''|起始日期|
|endDate|string/object|false|''|结束日期|


##Methods

###.setStartRange(date)
设置开始日期(默认显示值)

###.setEndRange(date)
设置结束日期（默认显示值）

###.getStartDate(callback)
获取起始日期值

###.getEndDate(callback)
获取结束日期值

###setStartDate(date)
设置起始日期日期选择框的起始日期

###setEndDate(date)
设置结束日期日期选择的结束日期






