## 查看文档数据

当你提交一个搜索请求，最近的 500 个搜索结果会显示在文档表格里。默认的，表格会显示当前选择的索引模式中定义的时间字段内容\(转换成本地时区\)以及 `_source` 文档。你可以从字段列表_添加字段到文档表格_。还可以用表格里包含的任意已建索引的字段来_排序列出的文档_。

要查看一个文档的字段数据，点击表格第一列\(通常都是时间\)文档内容左侧的 `Expand` 按钮 ![Expand Button](http://www.elasticsearch.org/guide/en/kibana/current/images/ExpandButton.jpg)。Kibana 从 Elasticsearch 读取数据然后在表格中显示文档字段。这个表格每行是一个字段的名字、过滤器按钮和字段的值。

![](/assets/import9.png)

1. 要查看原始 JSON 文档\(格式美化过的\)，点击 **JSON** 标签。
2. 要在单独的页面上查看文档内容，点击链接。你可以添加书签或者分享这个链接，以直接访问这条特定文档。
3. 收回文档细节，点击 **Collapse** 按钮 ![Collapse Button](http://www.elasticsearch.org/guide/en/kibana/current/images/CollapseButton.jpg)。





