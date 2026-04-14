# xiaoke-comparison

`xiaoke-comparison` 是一套为中文对比评测、厂商汇总、数据整理和选型参考内容设计的 Wenyan 自定义主题。

## 风格定位

- 清楚
- 克制
- 科技蓝
- 信息密度高
- 表格友好

## 适合内容

- 对比评测文章
- 厂商能力汇总
- 定价与套餐整理
- 工具选型参考
- 需要读者快速扫描表格和列表的内容

## 不追求的方向

- 不做情绪型长文风
- 不做强品牌感专栏风
- 不做大段抒情和氛围感视觉
- 不做装饰感过强的专题页

## 设计要点

1. 主色偏科技蓝，服务理性比较和信息分层
2. `h2` 用干净的下边线，不抢表格和正文的信息位置
3. 表格用了更明确的表头底色和隔行底色，方便移动端快速横向比
4. `blockquote` 只做结论提示，不做强情绪卡片
5. 图片边框和阴影更轻，避免正文视觉重心被配图抢走
6. 正文、列表、代码块和表格都优先服务“快速找信息”

## 和 xiaoke-default 的分工

- `xiaoke-default` 更适合方法论、系统分析和需要连续阅读的长文
- `xiaoke-comparison` 更适合对比、汇总和需要快速扫描的文章
- 如果一篇文章里表格和列表承担了主要阅读动作，优先用 `xiaoke-comparison`

## 使用方式

```bash
wenyan render -f tests/publish.md -c themes/xiaoke-comparison.css --no-mac-style
```

如果要发布：

```bash
wenyan publish -f article.md -c themes/xiaoke-comparison.css --no-mac-style
```
