### 博客+主题+网页
Hexo+NexT+GitHubPages

### 插件
- 订阅RSS
cnpm install hexo-generate-feed


hexo配置
plugins: hexo-generate-feed
feed: # RSS订阅插件
  type: atom
  path: atom.xml
  limit: 0
  
主题配置
rss: /atom.xml

- 压缩静态资源文件
cnpm install gulp --save

cnpm install gulp-minify-css --save
cnpm install gulp-uglify --save
cnpm install gulp-htmlmin --save
cnpm install gulp-htmlclean --save
cnpm install gulp-imagemin --save

创建根目录下的gulpfile.js文件

hexo g 后使用命令gulp

- 上传网页
cnpm install hexo-deployer-git --save

hexo配置
deploy:
  type: git
  repo: git@github.com:2694048168/2694048168.github.io.git
  branch: master
  
- gittalk评论设置
获取gittalk的ID和秘钥

CDN
  <link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/gitalk@1/dist/gitalk.css">
  <script src="https://cdn.jsdelivr.net/npm/gitalk@1/dist/gitalk.min.js"></script>

  <!-- or -->

  <link rel="stylesheet" href="https://unpkg.com/gitalk/dist/gitalk.css">
  <script src="https://unpkg.com/gitalk/dist/gitalk.min.js"></script>

配置主题
gitalk:
  enable: true
  github_id: 2694048168 
  repo: 2694048168.github.io
  client_id: aebff323e44f1516e521
  client_secret: 3934128e2a234e13b6118386667dee31ab703836
  admin_user: 2694048168
  distraction_free_mode: true 
  # Gitalk's display language depends on user's browser or system environment
  # If you want everyone visiting your site to see a uniform language, you can set a force language value
  # Available values: en | es-ES | fr | ru | zh-CN | zh-TW
  language: en | es-ES | fr | ru | zh-CN | zh-TW
  
- 本地搜索
# Local search
# Dependencies: https://github.com/theme-next/hexo-generator-searchdb