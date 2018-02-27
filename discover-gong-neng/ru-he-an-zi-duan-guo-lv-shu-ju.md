## 按字段过滤

你可以过滤搜索结果，只显示在某字段中包含了特定值的文档。也可以创建反向过滤器，排除掉包含特定字段值的文档。

你可以从字段列表或者文档表格里添加过滤器。当你添加好一个过滤器后，它会显示在搜索请求下方的过滤栏里。从过滤栏里你可以编辑或者关闭一个过滤器，转换过滤器\(从正向改成反向，反之亦然\)，切换过滤器开关，或者完全移除掉它。

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
  点击这个图标，可以在不移除过滤器的情况下关闭过滤条件。再次点击则重新打开。被禁用的过滤器是条纹状的灰色，要求包含\(相当于 Kibana3 里的 must\)的过滤条件显示为绿色，要求排除\(相当于 Kibana3 里的 mustNot\)的过滤条件显示为红色。
* 过滤器图钉 ![images/filter-pin.png](https://www.elastic.co/guide/en/kibana/current/images/filter-pin.png)
  点击这个图标_钉住_过滤器。被钉住的过滤器，可以横贯 Kibana 各个标签生效。比如在 _Visualize_ 标签页钉住一个过滤器，然后切换到 _Discover_ 或者 _Dashboard_ 标签页，过滤器依然还在。注意：如果你钉住了过滤器，然后发现检索结果为空，注意查看当前标签页的索引模式是不是跟过滤器匹配。
* 过滤器反转 ![images/filter-toggle.png](https://www.elastic.co/guide/en/kibana/current/images/filter-toggle.png)
  点击这个图标_反转_过滤器。默认情况下，过滤器都是包含型，显示为绿色，只有匹配过滤条件的结果才会显示。反转成排除型过滤器后，显示的是_不_匹配过滤器的检索项，显示为红色。
* 移除过滤器 ![images/filter-delete.png](https://www.elastic.co/guide/en/kibana/current/images/filter-delete.png)
  点击这个图标删除过滤器。
* 自定义过滤器 ![](https://www.elastic.co/guide/en/kibana/current/images/filter-custom.png)
  点击这个图标会打开一个文本编辑框。编辑框内可以修改 JSON 形式的过滤器内容：
  JSON 中可以灵活应用 bool query 组合各种 `should`、`must`、`must_not` 条件:
  ```
  {
    "query": {
      "match": {
        "at_names": {
          "query": "CCTV5",
          "type": "phrase"
        }
      }
    }
  }
  ```

![](/assets/import8.png)

