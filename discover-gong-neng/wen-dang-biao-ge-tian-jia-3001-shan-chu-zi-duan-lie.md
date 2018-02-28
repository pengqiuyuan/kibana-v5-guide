## 给文档表格添加字段列

默认的，文档表格会显示当前选择的索引模式中定义的时间字段内容\(转换成本地时区\)以及 `_source` 文档。你可以从字段列表添加字段到文档表格。

要添加字段列到文档表格：

1. 从字段列表中添加一列，移动鼠标到字段列表的字段上，点击它的 `add` 按钮
2. 从文档的字段数据添加一列，展开对应的文档后点击字段的![](https://www.elastic.co/guide/en/kibana/current/images/add-column-button.png)`Toggle column in table`按钮

添加的字段会替换掉文档表格里的 `_source` 列。同时还会显示在字段列表顶部的 `Selected Fields` 区域里。

要重排表格中的字段列，移动鼠标到你要移动的列顶部，点击移动过按钮。

![](/assets/import11.png)

## 从文档表格删除字段列

要从文档表格删除字段列：

1. 移动鼠标到字段列表的 `Selected Fields` 区域里你想要移除的字段上，然后点击它的 `remove` 按钮 ![Remove Field Button](http://www.elasticsearch.org/guide/en/kibana/current/images/RemoveFieldButton.jpg)。
2. 重复操作直到你移除完所有你想移除的字段。



