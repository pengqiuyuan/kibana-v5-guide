## 搜索数据

当你提交搜索的时候，直方图，文档表格，字段列表，都会自动反映成搜索的结果。hits\(匹配的文档\)总数会在直方图的右上角显示。文档表格显示前 500 个匹配文档。默认的，文档倒序排列，最新的文档最先显示。你可以通过点击时间列的头部来反转排序。

要搜索你的数据：

1. 在搜索框内输入请求字符串：

   * 简单的文本搜索，直接输入文本字符串。比如，如果你在搜索某个电影，你可以直接输入 `红海行动` 来过滤匹配到的文档。
   * 要搜索特定字段中的值，则在值前加上字段名。比如，你可以输入 `content_full:"红海行动"` 来限制搜索结果都是在 `content_full` 字段里有 `红海行动` 内容。
   * 要搜索一个值的范围，你可以用范围查询语法，`[START_VALUE TO END_VALUE]`。比如，要查找微博粉丝数 400 到 500 之间的，你可以输入 `follower_count:[400 TO 500]`。
   * 要指定更复杂的搜索标准，你可以用布尔操作符 `AND`, `OR`, 和 `NOT`。比如，微博粉丝数 400 到 500 之间的，并且过滤有特殊符号的`红海行动`数据，你可以输入 `(content_full:"红海行动" NOT (content_full:"《红海行动》" OR content_full:"红海行动|" OR content_full:"红海行动：") ) AND follower_count:[400 TO 500}`

   ![](/assets/import5.png)

点击回车键，或者点击 `Search` 按钮提交你的搜索请求。

**示例一：**

`content_full` 查找`红海行动`，查询语句 `content_full: "红海行动"`

![](/assets/import31.png)

**示例二：**

`content_full` 里查找含`红海行动`或者`捉妖记2`的文档，查询语句 `content_full: ("红海行动" OR "捉妖记2")`

![](/assets/import32.png)

**示例三：**

`content_full` 里查找含`红海行动`并且含`捉妖记2`的文档，查询语句 `content_full: ("红海行动" AND "捉妖记2")`

![](/assets/import33.png)

另一种查询语句

```
{"query_string" : { "fields" : ["content_full"],"query" : "\"红海行动\" AND \"捉妖记2\"" }}
```

![](/assets/import34.png)

**示例四：**

`content_full` 里查找含`红海行动`，`不含《红海行动》、红海行动|、红海行动：`，并且微博粉丝数在 `400` 到 `500` 之间的文档，查询语句：

```
(content_full:"红海行动" NOT (content_full:"《红海行动》" OR content_full:"红海行动|" OR content_full:"红海行动：") ) AND follower_count:[400 TO 500}
```

![](/assets/import35.png)

**示例五：**

```
follower_count:["400" TO "500"}  大于等于400小于500

follower_count:["400" TO "500"]  大于等于400小于等于500

follower_count:["400" TO *} 大于等于400
```



