# shihaiyang-world.github.io

### 层级逻辑
main分支：源代码
gh-pages分支：生成页面

配置github _config.yml中最下面的deploy配置
```yaml
deploy:
  type: 'git'
  repo: git@github.com:shihaiyang-world/shihaiyang-world.github.io.git
  branch: gh-pages  #生成的文件上传的分支
```


## 修改流程
每次修改main分支，执行hexo命令发布到gh-pages分支

```shell
hexo clean && hexo deploy
```

### 创建博客

```shell script
hexo new "My New Post"
```

### 创建静态文件
```shell script
hexo generate
hexo g
```

### 本地启动
```shell script
hexo server
hexo s
```

## 主题配置



## 开启评论

## 阅读时间

## 