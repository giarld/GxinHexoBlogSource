# GxinHexoBlogSource

## help
### 显示图片等资源
相对路径引用
{% asset_path slug %}
{% asset_img slug [title] %}
{% asset_link slug [title] %}
比如说：当你打开文章资源文件夹功能后，你把一个 example.jpg 图片放在了你的资源文件夹中，如果通过使用相对路径的常规 markdown 语法，它将 不会 出现在首页上。（但是它会在文章中按你期待的方式工作）

正确的引用图片方式是使用下列的标签插件而不是 markdown ：
{% asset_img example.jpg This is an example image %}

### 提交到github流程
``` bash
$ hexo clean
$ hexo generate
$ hexo deploy
```

### 本地服务器
``` bash
$ hexo server
```

### 可在page总插入HTML标签
