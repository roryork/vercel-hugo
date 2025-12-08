## 只需修改三处
* 全局站点配置：修改根目录下的config.toml文件
* 图片（logo等)：替换/docs/assets/images下的同名文件
* 站点内容修改：修改/data/目录下的yml文件
进入 Cloudflare Pages 目标项目 → 左侧「设置」→「构建与部署」；
点击「编辑构建命令和输出目录」；
强制配置：
Build command：hugo --gc --minify（必须填完整，不能留空 / 只填 hugo）；
Build output directory：dist（先保持 Hugo 默认值）；
Hugo 默认输出目录是 public，但如果你的项目配置里改了 publishDir，会导致输出目录不一致：
点击「保存」，然后顶部「部署」→「触发部署」→「从头开始重新构建」；
打开 GitHub 仓库 roryork/vercel-hugo，找到 Hugo 配置文件（config.toml/config.yaml/config.json）；
搜索 publishDir 字段：
Toml 格式：publishDir = "dist"（比如改成了 dist/docs 等）；
Yaml 格式：publishDir: dist；
