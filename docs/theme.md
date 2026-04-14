## theme：主题管理

主题管理，浏览内置主题、添加/删除自定义主题。

**列出主题：**

```bash
wenyan theme -l
```

**添加主题：**

```bash
# 添加本地 CSS 主题文件（推荐）
wenyan theme --add --name my-theme --path ./custom-theme.css

# 添加网络 CSS 主题文件（需确保网络可访问）
wenyan theme --add --name online-theme --path https://wenyan.yuzhi.tech/manhua.css
```

**删除主题：**

仅支持删除**自定义主题**，内置主题无法删除。

```bash
wenyan theme --rm my-theme
```

## 常用参数说明
| 参数              | 简写 | 说明                                                                 | 必填 | 默认值       |
|-------------------|------|----------------------------------------------------------------------|------|--------------|
| --list            | -l   | 列出所有可用主题（内置 + 自定义）                  | 否  | -            |
| --add            | -   | 触发添加自定义主题操作                   | 否（添加主题时必填）  | -            |
| --name            | -   | 自定义主题名称（唯一标识）                  | 是（仅 `--add` 生效时）  | -            |
| --path            | -   | 主题 CSS 文件路径（本地绝对 / 相对路径、网络 URL）                   |  是（仅 `--add` 生效时）  | -            |
| --rm            | -   | 删除指定名称的自定义主题                  | 否（删除主题时必填）  | -            |

---

## 当前自定义主题

这个仓库当前长期维护两套自定义主题。

| 主题 | 适合内容 | 风格关键词 | 主题文件 | 说明文档 |
|------|----------|------------|----------|----------|
| `xiaoke-default` | 方法论长文、系统分析、管理与技术交叉内容 | 冷静、清晰、耐读、轻品牌感 | `themes/xiaoke-default.css` | [xiaoke-default-theme.md](./xiaoke-default-theme.md) |
| `xiaoke-comparison` | 对比评测、厂商汇总、数据整理、选型参考 | 信息密度高、表格清楚、科技蓝、装饰更弱 | `themes/xiaoke-comparison.css` | [xiaoke-comparison-theme.md](./xiaoke-comparison-theme.md) |

## 选用建议

- 如果文章主价值来自判断推进、方法解释和长文阅读体验，优先用 `xiaoke-default`
- 如果文章主价值来自横向对照、表格扫描和信息检索效率，优先用 `xiaoke-comparison`
- 不要只按“好不好看”选主题，先看正文里的主阅读动作是连续阅读还是快速比较

## 常用命令

渲染预览：

```bash
wenyan render -f tests/publish.md -c themes/xiaoke-default.css --no-mac-style
wenyan render -f tests/publish.md -c themes/xiaoke-comparison.css --no-mac-style
```

发布时：

```bash
wenyan publish -f article.md -c themes/xiaoke-default.css --no-mac-style
wenyan publish -f article.md -c themes/xiaoke-comparison.css --no-mac-style
```
