## 按字段过滤

你可以过滤搜索结果，只显示在某字段中包含了特定值的文档。

要从字段列表添加过滤器：

1. 点击你想要过滤的字段名。会显示这个字段的前 5 名数据。每个数据的右侧，有两个小按钮 —— 一个用来添加常规\(正向\)过滤器，一个用来添加反向过滤器。
2. 要添加正向过滤器，点击 `Positive Filter` 按钮 ![Positive Filter Button](http://www.elasticsearch.org/guide/en/kibana/current/images/PositiveFilter.jpg)。这个会过滤掉在本字段不包含这个数据的文档。
3. 要添加反向过滤器，点击 `Negative Filter` 按钮 ![Negative Filter Button](http://www.elasticsearch.org/guide/en/kibana/current/images/NegativeFilter.jpg)。这个会过滤掉在本字段包含这个数据的文档。

![](/assets/import6.png)

要从文档表格添加过滤器：

1. 点击表格第一列\(通常都是时间\)文档内容左侧的 `Expand` 按钮 ![Expand Button](http://www.elasticsearch.org/guide/en/kibana/current/images/ExpandButton.jpg) 展开文档表格中的文档。每个字段名的右侧，有两个小按钮 —— 一个用来添加常规\(正向\)过滤器，一个用来添加反向过滤器。
2. 要添加正向过滤器，点击 `Positive Filter` 按钮 ![Positive Filter Button](http://www.elasticsearch.org/guide/en/kibana/current/images/PositiveFilter.jpg)。这个会过滤掉在本字段不包含这个数据的文档。
3. 要添加反向过滤器，点击 `Negative Filter` 按钮 ![Negative Filter Button](http://www.elasticsearch.org/guide/en/kibana/current/images/NegativeFilter.jpg)。这个会过滤掉在本字段包含这个数据的文档。

![](/assets/import7.png)

## 过滤器\(Filter\)的协同工作方式

在 Kibana 的任意页面创建过滤器后，就会在搜索输入框的下方，出现椭圆形的过滤条件。

鼠标移动到过滤条件上，会显示下面几个图标：

![images/filter-allbuttons.png](https://www.elastic.co/guide/en/kibana/current/images/filter-allbuttons.png)

* 过滤器开关 ![images/filter-enable.png](https://www.elastic.co/guide/en/kibana/current/images/filter-enable.png)
  点击这个图标，可以在不移除过滤器的情况下关闭过滤条件。再次点击则重新打开。

* 移除过滤器 ![images/filter-delete.png](https://www.elastic.co/guide/en/kibana/current/images/filter-delete.png)
  点击这个图标删除过滤器。

![](/assets/import8.png)



