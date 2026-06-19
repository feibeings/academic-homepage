# CLAUDE.md — 科研人员个人主页项目

## 项目规则

1. **称呼规则**：每次回复前必须使用"主人"作为称呼。
2. **不确定就先问**：遇到不确定的代码设计问题时，必须先询问主人，同时提出可选方案，不得直接行动。
3. **中文沟通**：与主人的对话使用中文。
4. **虚拟环境**：所有 Python 代码需在项目虚拟环境 `website_env` 中运行。使用前激活：
   - Windows: `website_env\Scripts\activate`
   - Git Bash: `source website_env/Scripts/activate`

## AI 行为规范

1. 先思考再编码 — 明确陈述假设；不确定时先问
2. 简洁优先 — 不添加未要求的功能、不做未要求的抽象
3. 精准修改 — 不"改进"相邻代码，匹配现有代码风格
4. 目标驱动执行 — 将指令转化为可验证目标

## 项目信息

- **网站地址**：https://jiangfei-cv.pages.dev
- **GitHub 仓库**：github.com/feibeings/academic-homepage
- **模板**：al-folio (Jekyll + Material Design)
- **托管**：Cloudflare Pages（自动部署，每次 git push 触发）
- **构建命令**：`bundle exec jekyll build`，输出目录 `_site`
- **PDF/Word 简历**：GitHub Actions 自动从 `cv.md` 生成

## 关键文件

| 用途 | 文件路径 |
|------|---------|
| 网站配置 | `_config.yml` |
| 首页/关于我 | `_pages/about.md` |
| 论文数据库 | `_bibliography/papers.bib` |
| 项目展示 | `_projects/*.md` |
| 专利页面 | `_pages/patents.md` |
| 获奖页面 | `_pages/awards.md` |
| 学生页面 | `_pages/students.md` |
| 简历页（隐藏） | `_pages/cv.md` |
| 简历 Web 数据 | `_data/cv.yml` |
| 简历 PDF 源 | `cv.md` |
| Cloudflare 部署 | `.github/workflows/deploy-cloudflare.yml` |
| PDF 生成 | `.github/workflows/build-cv.yml` |

## 修改后更新网站

```bash
git add -A
git commit -m "描述修改内容"
git push
# 等待 1-3 分钟自动部署
```

## 导航栏

公开页面：论文发表(2) → 指导学生(3) → 科研项目(4) → 专利(5) → 获奖荣誉(7)
隐藏页面：个人简历(/cv/)、博客(1)

## 用户信息

- 姓名：蒋飞
- 邮箱：jiangfei@dgut.edu.cn
- 单位：东莞理工学院 机械工程学院
- 职称：准聘副教授
- 研究方向：深度学习/大模型故障诊断、机器视觉缺陷检测、动力学建模与信号处理
