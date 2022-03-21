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

### 推送
```shell script
hexo clean && hexo g -d
```

## 主题配置

使用next的方式
```shell script
$ cd hexo-site
$ git clone https://github.com/next-theme/hexo-theme-next themes/next

$ cd hexo-site
$ cd themes/next
$ git pull origin master

```
在修改_config.yml
```yaml
theme: next
```

设置风格
/themes/next/_config.yml 
```shell script
scheme: Gemini
```

参考：https://theme-next.js.org/docs/getting-started/


## 开启评论

使用valine评论系统： https://qianfanguojin.top/2022/01/20/Hexo%E5%8D%9A%E5%AE%A2%E8%BF%9B%E9%98%B6%EF%BC%9A%E4%B8%BA-Next-%E4%B8%BB%E9%A2%98%E6%B7%BB%E5%8A%A0-Waline-%E8%AF%84%E8%AE%BA%E7%B3%BB%E7%BB%9F/
```yaml
valine:
  enable: true # 是否开启
  appid:   # 上一步获取的 App ID
  appkey:  # 上一步获取的 App Key
  notify: false # 新留言是否需要通知 https://github.com/xCss/Valine/wiki
  verify: false # 是否需要验证，验证比较反人类建议false关闭
  placeholder: 请在此输入您的留言 # 默认留言框内的文字
  avatar: mm # 默认头像
  guest_info: nick,mail # 默认留言框的头部需要访问者输入的信息
  pageSize: 10 # pagination size #默认单页的留言条数
```

## 阅读时间
```shell script
npm install hexo-word-counter
hexo clean
```

/themes/next/_config.yml 
```yaml
# 文章字数统计
symbols_count_time:
  symbols: true
  time: true
  total_symbols: true
  total_time: true
  exclude_codeblock: false
  awl: 4
  wpm: 275
  suffix: "mins."
```
参考：https://github.com/next-theme/hexo-word-counter

## 