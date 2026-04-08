# 数据分析参考书 Wiki

这是一个基于 Quarto 的静态参考站，目标是把常见的数据分析任务拆成可直接查阅的页面：给出最小示例、真实使用场景、相关函数/公式和注意事项。

## 本地运行

确保当前 shell 能访问 Quarto：

```bash
PATH=/usr/local/bin:/opt/homebrew/bin:$PATH quarto preview
```

构建静态站：

```bash
PATH=/usr/local/bin:/opt/homebrew/bin:$PATH quarto render
```

## 内容组织

- `scenes/`：按实际工作场景查
- `python/`：pandas / NumPy 高频索引
- `excel/`：Excel 高频公式索引
- `compare/`：同一任务的 Python / Excel 对照
- `cases/`：小案例入口
- `templates/`：后续新增页面时可复用的模板

## 内容规则

- 公开内容只放原创总结、示例和索引。
- 不放可替代原书阅读的长篇重写内容。
- 每个参考页优先回答“这个问题怎么立刻解决”。

## 发布

推送到 `main` 后，GitHub Actions 会构建 `_site/` 并发布到 GitHub Pages。
