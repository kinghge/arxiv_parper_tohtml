# ArXiv论文HTML生成器

这是一个用于自动获取ArXiv论文并生成HTML页面展示的工具。该工具可以帮助研究人员追踪特定领域的最新论文，并以友好的方式展示论文信息。

## 功能特点

- 自动从ArXiv获取指定主题的最新论文
- 支持自定义关键词和过滤条件
- 生成美观的HTML页面展示论文信息
- 显示论文作者、摘要、链接等详细信息
- 支持论文代码仓库链接的自动获取
- 可配置的展示选项（标题、作者、徽章等）

## 安装要求

- Python 3.6+
- 依赖包：
  - requests
  - arxiv
  - pyyaml

## 安装方法

1. 克隆仓库：
```bash
git clone https://github.com/kinghge/arxiv_parper_tohtml.git
cd arxiv_paper_tohtml
```

2. 安装依赖：
```bash
pip install -r requirements.txt
```

## 配置说明

在`config.yaml`文件中配置以下参数：

```yaml
user_name: "your_github_username"
repo_name: "your_repo_name"
show_authors: true
show_links: true
show_badge: true
max_results: 10

publish_html: true

json_readme_path: "./docs/arxiv-daily.json"
path: "./docs/index.html"

keywords:
  "Your Topic":
    filters: ["keyword1", "keyword2"]
```

## 使用方法

1. 修改`config.yaml`配置文件，设置你感兴趣的研究领域和关键词

2. 运行脚本：
```bash
python arxivpaper_html.py
```

3. 生成的HTML文件将保存在配置文件指定的路径中

## 主要功能

- `load_config()`: 加载配置文件
- `get_daily_papers()`: 获取每日最新论文
- `get_code_link()`: 获取论文相关的代码仓库链接
- `json_to_html()`: 将论文数据转换为HTML页面

## 许可证

本项目采用 MIT 许可证 - 详见 [LICENSE](LICENSE) 文件

## 贡献

欢迎提交问题和改进建议！如果你想贡献代码：

1. Fork 本仓库
2. 创建你的特性分支
3. 提交你的改动
4. 推送到你的分支
5. 创建一个新的Pull Request
