## 搜索数据

在 Discover 页提交一个搜索，你就可以搜索匹配当前索引模式的索引数据了。你可以直接输入简单的请求字符串，也就是用 Lucene [query syntax](https://lucene.apache.org/core/2_9_4/queryparsersyntax.html)，也可以用完整的基于 JSON 的 [Elasticsearch Query DSL](http://www.elasticsearch.org/guide/en/elasticsearch/reference/current/query-dsl.html)。

当你提交搜索的时候，直方图，文档表格，字段列表，都会自动反映成搜索的结果。hits\(匹配的文档\)总数会在直方图的右上角显示。文档表格显示前 500 个匹配文档。默认的，文档倒序排列，最新的文档最先显示。你可以通过点击时间列的头部来反转排序。事实上，所有建了索引的字段，都可以用来排序，稍后会详细说明。

要搜索你的数据：

1. 在搜索框内输入请求字符串：
   * 简单的文本搜索，直接输入文本字符串。比如，如果你在搜索网站服务器日志，你可以输入 `safari` 来搜索各字段中的 `safari` 单词。
   * 要搜索特定字段中的值，则在值前加上字段名。比如，你可以输入 `status:200` 来限制搜索结果都是在 `status` 字段里有 `200` 内容。
   * 要搜索一个值的范围，你可以用范围查询语法，`[START_VALUE TO END_VALUE]`。比如，要查找 4xx 的状态码，你可以输入 `status:[400 TO 499]`。
   * 要指定更复杂的搜索标准，你可以用布尔操作符 `AND`, `OR`, 和 `NOT`。比如，要查找 4xx 的状态码，还是 `php` 或 `html` 结尾的数据，你可以输入 `status:[400 TO 499] AND (extension:php OR extension:html)`。

> 这些例子都用了 Lucene query syntax。你也可以提交 Elasticsearch Query DSL 式的请求。更多示例，参见之前 [Elasticsearch 章节](../../elasticsearch/api/search.md)。

2. 点击回车键，或者点击 `Search` 按钮提交你的搜索请求。

