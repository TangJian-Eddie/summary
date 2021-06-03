清空 DatePicker（日期选择器）的方法：

```javascript
this.$refs.element.handleClear();
```

清空 TimePicker（时间选择器）的方法：

```javascript
this.$refs.element.handleClear();
```

清空 Select 组件的方法：

```javascript
this.$refs.element.clearSingleSelect();
```

清空 Table 组件的方法：

```javascript
this.$refs.element.selectAll(flase);
```

promise.all 和 Table 的@on-select、@on-selection-change 结合实现批量删除

利用 Modal 的 on-visible-change 事件实现增加和修改（深拷贝）

利用 select 的 label-in-value 实现两个输入框的绑定

利用 select 的远程搜索实现输入

select 的远程搜索结合实现两个输入框的绑定以及增改

利用 Table 的 render 实现图片、替换

时间格式化

表单校验 date 格式

select 数据类型 number 的 bug，以及 number 的表单校验
