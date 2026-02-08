## [Available commands](https://github.com/medialab/xan?tab=readme-ov-file#available-commands)

### 探索与可视化

- [count (c)](https://github.com/medialab/xan/blob/master/docs/cmd/count.md)  统计文件中的行数
- [headers (h)](https://github.com/medialab/xan/blob/master/docs/cmd/headers.md)  显示头部名称
- [view (v)](https://github.com/medialab/xan/blob/master/docs/cmd/view.md)  以人类友好的方式预览 CSV 文件
- [flatten](https://github.com/medialab/xan/blob/master/docs/cmd/flatten.md)  显示文件每一行的扁平化版本
- [hist](https://github.com/medialab/xan/blob/master/docs/cmd/hist.md)  打印以 CSV 文件行作为柱状图的直方图
- [plot](https://github.com/medialab/xan/blob/master/docs/cmd/plot.md)  绘制散点图或折线图
- [heatmap](https://github.com/medialab/xan/blob/master/docs/cmd/heatmap.md)  绘制 CSV 矩阵的热图
- [progress](https://github.com/medialab/xan/blob/master/docs/cmd/progress.md)  在读取 CSV 数据时显示进度条

### 搜索与过滤

- [search](https://github.com/medialab/xan/blob/master/docs/cmd/search.md)  在 CSV 数据中搜索（或替换）模式
- [filter](https://github.com/medialab/xan/blob/master/docs/cmd/filter.md)  基于评估表达式只保留一些 CSV 行
- [head](https://github.com/medialab/xan/blob/master/docs/cmd/head.md)  CSV 文件的前几行
- [tail](https://github.com/medialab/xan/blob/master/docs/cmd/tail.md)  CSV 文件的最后几行
- [slice](https://github.com/medialab/xan/blob/master/docs/cmd/slice.md)  切片 CSV 文件的行
- [top](https://github.com/medialab/xan/blob/master/docs/cmd/top.md)  根据某一列查找 CSV 文件的顶部行
- [sample](https://github.com/medialab/xan/blob/master/docs/cmd/sample.md)  随机抽样 CSV 数据

### 排序与去重

- [sort](https://github.com/medialab/xan/blob/master/docs/cmd/sort.md)  排序 CSV 数据
- [dedup](https://github.com/medialab/xan/blob/master/docs/cmd/dedup.md)  去重 CSV 文件
- [shuffle](https://github.com/medialab/xan/blob/master/docs/cmd/shuffle.md)  随机打乱 CSV 数据

### 聚合

- [frequency (freq)](https://github.com/medialab/xan/blob/master/docs/cmd/frequency.md)  显示频率表
- [groupby](https://github.com/medialab/xan/blob/master/docs/cmd/groupby.md)  按 CSV 文件的组聚合数据
- [stats](https://github.com/medialab/xan/blob/master/docs/cmd/stats.md)  计算基本统计信息
- [agg](https://github.com/medialab/xan/blob/master/docs/cmd/agg.md)  聚合 CSV 文件中的数据
- [bins](https://github.com/medialab/xan/blob/master/docs/cmd/bins.md)  将数值列划分为多个区间
- [window](https://github.com/medialab/xan/blob/master/docs/cmd/window.md)  计算窗口聚合（累加和、滚动均值、滞后等）

### 合并多个 CSV 文件

- [cat](https://github.com/medialab/xan/blob/master/docs/cmd/cat.md)  按行或列连接
- [join](https://github.com/medialab/xan/blob/master/docs/cmd/join.md)  合并 CSV 文件
- [fuzzy-join](https://github.com/medialab/xan/blob/master/docs/cmd/fuzzy-join.md)  用含有模式（例如正则表达式）的另一个 CSV 文件合并
- [merge](https://github.com/medialab/xan/blob/master/docs/cmd/merge.md)  合并多个相似的已排序 CSV 文件

### 添加、转换、删除及移动列

- [select](https://github.com/medialab/xan/blob/master/docs/cmd/select.md)  从 CSV 文件中选择列
- [drop](https://github.com/medialab/xan/blob/master/docs/cmd/drop.md)  从 CSV 文件中删除列
- [map](https://github.com/medialab/xan/blob/master/docs/cmd/map.md)  通过评估每个 CSV 行的表达式创建新列
- [transform](https://github.com/medialab/xan/blob/master/docs/cmd/transform.md)  通过评估每个 CSV 行的表达式转换列
- [enum](https://github.com/medialab/xan/blob/master/docs/cmd/enum.md)  通过在前面添加索引列来枚举 CSV 文件
- [flatmap](https://github.com/medialab/xan/blob/master/docs/cmd/flatmap.md)  每个 CSV 行评估的表达式返回的每个值生成一行
- [fill](https://github.com/medialab/xan/blob/master/docs/cmd/fill.md)  填充空单元格
- [blank](https://github.com/medialab/xan/blob/master/docs/cmd/blank.md)  将连续相同的单元格值变为空白

### 格式化、转换与重组

- [behead](https://github.com/medialab/xan/blob/master/docs/cmd/behead.md)  从 CSV 文件中删除头部
- [rename](https://github.com/medialab/xan/blob/master/docs/cmd/rename.md)  重命名 CSV 文件的列
- [input](https://github.com/medialab/xan/blob/master/docs/cmd/input.md)  读取格式异常的 CSV 数据
- [fixlengths](https://github.com/medialab/xan/blob/master/docs/cmd/fixlengths.md)  使所有行具有相同长度
- [fmt](https://github.com/medialab/xan/blob/master/docs/cmd/fmt.md)  格式化 CSV 输出（改变字段分隔符）
- [explode](https://github.com/medialab/xan/blob/master/docs/cmd/explode.md)  基于某列分隔符爆炸行
- [implode](https://github.com/medialab/xan/blob/master/docs/cmd/implode.md)  根据分歧列合并连续相同的行
- [from](https://github.com/medialab/xan/blob/master/docs/cmd/from.md)  将多种格式转换为 CSV
- [to](https://github.com/medialab/xan/blob/master/docs/cmd/to.md)  将 CSV 文件转换为多种数据格式
- [scrape](https://github.com/medialab/xan/blob/master/docs/cmd/scrape.md)  将 HTML 抓取为 CSV 数据
- [reverse](https://github.com/medialab/xan/blob/master/docs/cmd/reverse.md)  反转 CSV 数据的行
- [transpose (t)](https://github.com/medialab/xan/blob/master/docs/cmd/transpose.md)  转置 CSV 文件

### 将 CSV 文件拆分为多个部分

- [split](https://github.com/medialab/xan/blob/master/docs/cmd/split.md)  将 CSV 数据拆分为块
- [partition](https://github.com/medialab/xan/blob/master/docs/cmd/partition.md)  根据列值对 CSV 数据进行分组

### 并行化

- [parallel (p)](https://github.com/medialab/xan/blob/master/docs/cmd/parallel.md)  类似于 Map-Reduce 的并行计算

### 生成 CSV 文件

- [range](https://github.com/medialab/xan/blob/master/docs/cmd/range.md)  从数值范围创建 CSV 文件

### 执行副作用

- [eval](https://github.com/medialab/xan/blob/master/docs/cmd/eval.md)  评估/调试单个表达式
- [foreach](https://github.com/medialab/xan/blob/master/docs/cmd/foreach.md)  循环遍历 CSV 文件以执行副作用

### 词法计量与模糊匹配

- [tokenize](https://github.com/medialab/xan/blob/master/docs/cmd/tokenize.md)  对文本列进行分词
- [vocab](https://github.com/medialab/xan/blob/master/docs/cmd/vocab.md)  基于标记化文档构建词汇
- [cluster](https://github.com/medialab/xan/blob/master/docs/cmd/cluster.md)  聚类 CSV 数据以查找近似重复项

### 矩阵与网络相关命令

- [matrix](https://github.com/medialab/xan/blob/master/docs/cmd/matrix.md)  将 CSV 数据转换为矩阵数据
- [network](https://github.com/medialab/xan/blob/master/docs/cmd/network.md)  将 CSV 数据转换为网络数据
