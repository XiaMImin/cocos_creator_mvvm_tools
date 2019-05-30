## VM Label

### 介绍 

VM组件文本监听，用于处理 Label 的监听问题。监听watchPath  路径 数值的变动情况，变动Label文本内容。使用模板模式，还可以将输入的字符串格式化。可以监听多路径，来同时在一个label上显示多个数据源的信息。

### 属性



### 模板解析

使用 {{0}} {{1}} {{2}} 方式设置模板内容（设置label 的默认值）。在运行时，会动态的将对应位置的 watchPath 替换到其中。你可以额外添加修饰符号来格式化信息源，比如 {{0:int}} 会将数字内容以整数显示，{{0:time}} 以时间格式显示时间戳 等。

以下是目前支持的格式化内容: 

int - 只显示整数部分
% - 显示百分比
fix(0) -显示小数位数
t - 显示为计时器格式(00：00：00)