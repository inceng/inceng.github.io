## 本博客地址 https://inceng.github.io/

代码托管于Github，博客自豪地采用hexo构建。

## 常用hexo命令

```
npm install hexo -g #安装  
npm update hexo -g #升级  
hexo init #初始化
hexo clean #清除生成的静态文件

hexo n "我的博客" == hexo new "我的博客" #新建文章
hexo p == hexo publish
hexo g == hexo generate #生成静态文件
hexo s == hexo server #启动本地服务，http://localhost:4000预览
hexo d == hexo deploy #部署到远程Github
```

本地搭建hexo发布博客系统要点：
1.安装nodeJs 和 Git （下载最新版即可）。
2.本地仓库和Github仓库关联步骤，ssh本地生成然后拷贝id_rsa.pub内容至Github仓库。
2.npm安装hexo包(有可能会hexo cannot found的报错,配置hexo的环境变量即可)
3.配置_config.yml中Github仓库地址，安装hexo依赖模块。
```
deploy:
  type: git
  repo: https://github.com/chxuan/chxuan.github.io.git
  branch: master
```
```
npm install hexo-deployer-git --save
```
