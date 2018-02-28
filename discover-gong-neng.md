# discover 功能

Discover 标签页用于交互式探索你的数据。你可以访问到匹配得上你选择的索引模式的每个索引的每条记录。你可以提交搜索请求，过滤搜索结果，然后查看文档数据。你还可以看到匹配搜索请求的文档总数，获取字段值的统计情况。如果索引模式配置了时间字段，文档的时序分布情况会在页面顶部以柱状图的形式展示出来。

![](/assets/QQ20180227-162706.png)  

## 开始一个新的搜索

要清除当前搜索或开始一个新搜索，点击 Discover 工具栏的 New Search 按钮。

## 保存搜索

你可以在 Discover 页加载已保存的搜索，也可以用作 [visualizations](./visualize.md) 的基础。保存一个搜索，意味着同时保存下了搜索请求字符串和当前选择的索引模式。

要保存当前搜索：

1. 点击 Discover 工具栏的 `Save Search` 按钮。
2. 输入一个名称，点击 `Save`。

## 加载一个已存搜索

要加载一个已保存的搜索：

1. 点击 Discover 工具栏的 `Load Search` 按钮。
2. 选择你要加载的搜索。

如果已保存的搜索关联到跟你当前选择的索引模式不一样的其他索引上，加载这个搜索也会切换当前的已选索引模式。

## 改变你搜索的索引

当你提交一个搜索请求，匹配当前的已选索引模式的索引都会被搜索。当前模式模式会显示在搜索栏下方。要改变搜索的索引，需要选择另外的模式模式。

要选择另外的索引模式：

1. 点击 Discover 工具栏的 `Settings` 按钮。
2. 从索引模式列表中选取你打算采用的模式。

关于索引模式的更多细节，请阅读稍后 [Setting 功能小节](./settings.md)。

## 自动刷新页面

亦可以配置一个刷新间隔来自动刷新 Discover 页面的最新索引数据。这会定期重新提交一次搜索请求。

设置刷新间隔后，会显示在菜单栏时间过滤器的左边。

要设置刷新间隔：

1. 点击菜单栏右上角的 `Time Picker` ![Time Picker](https://www.elastic.co/guide/en/kibana/current/images/time-picker.jpg)。
2. 点击 `Auto refresh` 标签。
3. 从列表中选择一个刷新间隔。

![images/autorefresh-intervals.png](https://www.elastic.co/guide/en/kibana/current/images/autorefresh-intervals.png)

开启自动刷新后，Kibana 的顶部栏会出现一个暂停按钮和自动刷新的间隔，点击 **Pause** 按钮可以暂停自动刷新。



想要对当前页所有过滤器统一执行上面的某个操作，点击 **Actions** 按钮，然后再执行操作即可。









