## 2026-04-08 13:26
- Did: 初始化 Quarto 参考书 Wiki，完成首页、开始使用、5 个场景页、Python/Excel 索引、对照页、案例库、更新日志、页面模板和 GitHub Pages 工作流。
- Commands: `quarto create-project <repo> --type website`; `git init -b main`; `mkdir -p scenes python excel compare cases templates docs .github/workflows`; `quarto render`; `quarto preview --no-browser --no-watch-inputs --timeout 5`
- Result: 站点成功渲染到 `_site/`，本地预览服务可启动；模板页已从正式渲染范围排除；公开仓库不记录本地 PDF 绝对路径。
- Next: 用你提供的两本本地 PDF 继续补“筛选、排序、去重”“文本拆分与提取”“查找匹配与关联”等下一批参考页。

## 2026-04-08 14:32
- Did: 基于两本本地 PDF 抽取章节结构，新增 5 个场景页、2 个书籍地图页、2 个书中案例页，并扩展首页、场景索引、Python/Excel 索引和更新日志。
- Commands: `python3.12 + fitz/pdfplumber` 提取两本 PDF 的目录和案例主题；`quarto render`; `rm -rf _site`; `rg ... _site/search.json`
- Result: 站点成功渲染 22 个页面；搜索索引可检索“Power Query”“MovieLens”“筛选、排序、去重”“TEXTBEFORE”“merge()”等新增内容；临时复制进 repo 的 PDF 已删除。
- Next: 继续按书中主题补时间序列、滚动窗口、Power Query 深入、Power Pivot、假设分析与 Solver、自动化相关页面。

## 2026-04-08 14:45
- Did: 继续基于两本 PDF 扩展站点，新增 12 个专题页，覆盖 Python 的基础工作流、数据加载/API、清洗合并、时间序列、建模、Advanced NumPy、IPython 提效，以及 Excel 的工作簿/表格、公式模式、数据验证与保护、链接汇总、Analysis ToolPak、Power Query、Power Pivot、假设分析、自动化。
- Commands: `python3.12 + fitz` 提取 Excel 27/28/31-44 章和 Python 11/12/附录主题；`quarto render`; `rg ... _site/search.json`
- Result: 站点成功渲染 38 个页面；搜索索引可检索“滚动窗口”“Power Pivot”“Goal Seek”“Solver”“Office Scripts”“Numba”“Analysis ToolPak”“数据加载、API”等专题；导航、书籍地图和索引页都已连到新专题页。
- Next: 继续把两本书中尚未单独拆页的零散章节补成参考页，优先补 Excel 图表细分、数据验证/模板实战，以及 Python 分类数据、层次索引、统计与案例细化。

## 2026-04-08 14:59
- Did: 新增 10 个更偏实战的细分页，覆盖 Excel 的选图与汇报图表、模板与打印、数据验证、界面提效、动态数组、条件格式、迷你图/数字格式、分组大纲，以及 Python 的分类数据、层次索引、统计摘要；新增 2 个更贴近工作流的案例页，并把索引、书籍地图、案例入口全部接通。
- Commands: `python3.12 + fitz` 提取 Excel 7/17/18/22 章的实战子主题；`quarto render`; `rg ... _site/search.json`
- Result: 站点成功渲染 51 个页面；搜索索引已收录“动态数组与数组公式实战”“条件格式实战”“迷你图、数字格式与表内可视化”“分组大纲与结构化报表”“分类数据实战”“层次索引实战”等新页。
- Next: 如果继续追求更接近“全书完整覆盖”，下一轮可把剩余零散点拆成更小的参考页，例如 Excel 的 Comments/Notes/Shapes、保护与共享细节、VBA 自定义函数案例，以及 Python 的字符串正则案例、JSON/HTML 抓取案例、GroupBy 应用案例等。

## 2026-04-08 15:07
- Did: 继续补剩余边角实战页，新增 Python 的字符串与正则、重塑与透视、GroupBy/apply 配方，以及 Excel 的批注备注、保护与交付、VBA 自定义函数、控件与事件专题，并将这些内容接入索引、书籍地图和案例入口。
- Commands: `python3.12 + fitz` 提取 Excel 4/30/39/41/42/43 章和 Python 7.4/8.3/10.3/13.x 主题；`quarto render`; `rg ... _site/search.json`
- Result: 站点成功渲染 58 个页面；搜索索引已收录“字符串与正则实战”“重塑与透视实战”“GroupBy / apply 实战配方”“批注、备注与协作标记实战”“保护、检查与交付实战”“VBA 自定义函数实战”“控件、事件与交互工作表”等新页。
- Next: 如果继续往“尽量全书化”推进，下一轮可再补 Excel 的 Shapes/Images/绘图细节、评论协作模板案例、Add-In 打包案例，以及 Python 的 API/HTML 抓取独立案例、时间序列业务案例和建模前特征工程案例。

## 2026-04-08 15:19
- Did: 新增 5 个进一步贴近日常工作的专题页和 1 个案例页，覆盖 Python 的 JSON/API/网页表格抓取、时间序列业务案例、建模前特征工程，以及 Excel 的形状/图片报表润色、Add-In 打包与分发，并把这些页接入导航、索引、书籍地图、案例库和更新日志。
- Commands: `python3.12 + fitz` 提取 Excel 第 20/43 章与 Python 第 6.1/6.3/11.6/11.7/12.1/12.2/13.1/13.3 节目录；`quarto render`; `rg ... _site/search.json`; `find _site -name '*.html' | wc -l`
- Result: 站点成功渲染 64 个 HTML 页面；搜索索引已收录“JSON、API 与网页表格抓取实战”“时间序列业务案例”“建模前特征工程实战”“形状、图片与报表润色实战”“Add-In 打包与分发实战”“从 API 抓取到特征表”等新内容。
- Next: 继续把两本书剩余的中低频工作流拆成更细的小页，优先补 Excel 的外部数据连接/共享细节与 Python 的书中案例再细化。

## 2026-04-08 15:23
- Did: 继续细化书中案例和 Excel 数据来源工作流，新增 Excel 的外部数据连接与刷新实战页，以及 Python 第 13 章的 Bitly、MovieLens、婴儿名字三个单独案例页，并将它们接入侧边栏、书籍地图、案例库和总案例页。
- Commands: `python3.12 + fitz` 提取 Excel 第 21/34/35/37 章和 Python 第 13 章目录；`quarto render`; `rg ... _site/search.json`; `find _site -name '*.html' | wc -l`
- Result: 站点成功渲染 68 个 HTML 页面；搜索索引已收录“Bitly 日志时区分析”“MovieLens 评分差异分析”“婴儿名字长期趋势分析”“外部数据连接与刷新实战”“Queries & Connections”“Refresh All”等新内容。
- Next: 继续把 Python 第 13 章剩余的 USDA / FEC 案例与 Excel 的更多共享分发细节拆成页，进一步逼近“全书可查”状态。

## 2026-04-08 15:31
- Did: 本地启动 Quarto 预览服务并做了一轮访问检查；同时把 GitHub Pages 工作流从“push 到 main 自动部署”改为“仅手动触发”，避免误发布公开页面。
- Commands: `quarto preview --no-browser --port 4173 --host 127.0.0.1`; `curl http://127.0.0.1:4173/...`; `rg ... _site/search.json`; `sed -n '1,220p' .github/workflows/publish.yml`
- Result: 本地预览地址可用；首页、Python 索引、Excel 索引、案例库、对照页和搜索索引均返回 `200`；首页关键导航文案命中正常；Pages 工作流已改成仅 `workflow_dispatch` 手动触发。
- Next: 等你本地看过页面后，再决定是否继续做视觉修整或恢复发布流程。

## 2026-04-08 15:44
- Did: 排查了页面顶部出现的 “Render + 输入框” 问题，确认它来自 `quarto preview` 注入的本地开发预览脚本，而不是站点本身；改用纯静态 HTTP 服务供本地预览。
- Commands: `curl http://127.0.0.1:4173/python/index.html`; `rg 'quarto-preview|inputFile|watchInputFile'`; `python3 -m http.server 4174 --bind 127.0.0.1`; `curl http://127.0.0.1:4174/...`; `lsof -ti tcp:4173`; `lsof -ti tcp:4174`
- Result: 静态构建文件中不含 `quarto-preview.js`；本地静态地址 `http://127.0.0.1:4174/` 返回 `200`，首页和子页面可访问，且不再包含预览工具条；4173 预览端口已不再占用，4174 静态服务仍在运行。
- Next: 等你在 4174 看页面；如果没问题，再决定是继续本地交付，还是改成别的私有托管方式。

## 2026-04-08 16:03
- Did: 参考 `queueupenglish` 的最简静态发布方式完成上线前检查；对源码和构建产物做了 API / token / 本地路径扫描；创建 GitHub 仓库、推送 `main`、启用 GitHub Pages，并修复首次部署所需的 Pages workflow 配置。
- Commands: `rg` 扫描源码与 `_site`；`gitleaks detect --no-git`; `gh auth status`; `gh repo create liuzhiqi71/data-skills-wiki --public`; `git push`; `gh api -X POST repos/liuzhiqi71/data-skills-wiki/pages -f build_type=workflow`; `gh workflow run publish.yml`; `gh run watch ...`; `curl -I https://liuzhiqi71.github.io/data-skills-wiki/`
- Result: 未发现 API key、token、凭证或本地路径泄露；仓库已发布到 GitHub，Pages 已通过 workflow 成功部署；线上地址 `https://liuzhiqi71.github.io/data-skills-wiki/` 返回 `200`，首页关键导航文案命中正常。
- Next: 如果后续还要继续更新内容，直接在本仓库提交并按需手动触发 `publish.yml` 即可。
