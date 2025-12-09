* 全局站点配置：修改根目录下的config.toml文件
* 图片（logo等)：替换/docs/assets/images下的同名文件
* 站点内容修改：修改/data/目录下的yml文件
* 进入 Cloudflare Pages 目标项目 → 左侧「设置」→「构建与部署」；
* 点击「编辑构建命令和输出目录」；
* 强制配置：
  Build command：hugo --gc --minify（必须填完整，不能留空 / 只填 hugo）；
  Build output directory：docs（先保持 Hugo 默认值）；
* 删除左小角广告
  github搜索文件"sidebar.html"，里面有个iframe，删除从 < li > 到 </li> 的整个部分，包括其中的iframe
