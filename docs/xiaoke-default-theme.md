# xiaoke-default

`xiaoke-default` 是一套为中文方法论长文、系统分析文、管理与技术交叉内容设计的 Wenyan 自定义主题。

## 风格定位

- 冷静
- 清晰
- 可信
- 轻品牌感
- 长文耐读

## 适合内容

- 方法论文章
- 架构理解
- 系统边界解释
- 管理与技术交叉分析
- 系列化公众号写作

## 不追求的方向

- 不做情绪鸡汤风
- 不做营销海报风
- 不做重装饰杂志风
- 不做极客终端风

## 设计要点

1. `h1` 用稳重下边线，避免封面标题感过强
2. `h2` 用轻底色和左侧强调线，突出结构分段
3. `blockquote` 更像判断结论块，而不是花哨引用框
4. 列表、代码块、表格都优先服务信息组织
5. 整体颜色偏蓝灰和青绿色，适合长期专栏输出

## 使用方式

```bash
wenyan render -f tests/publish.md -c themes/xiaoke-default.css --no-mac-style
```

如果要发布：

```bash
wenyan publish -f article.md -c themes/xiaoke-default.css --no-mac-style
```
