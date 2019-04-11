# YuFy1314.github.io yufy-Theme Readme

该文档是从[Miccall](https://github.com/miccall)处fork过来的, 主题layout没变, 一些细节经过更改:

#### 文中哪些不懂的地方可以参考[hexo官方文档](https://hexo.io/zh-cn/), 也可以[new issue](https://github.com/YuFy1314/YuFy1314.github.io/issues/new)

## Demo 演示

个人网站 : [YuFy1314](https://yufy1314.github.io/)

主题主页: 
<p align="center">
  <a href="#"><img src="https://github.com/YuFy1314/YuFy1314.github.io/blob/MiccallTheme/source/images/Home_01.png?raw=true" alt="Version"></a>
   <a href="#"><img src="https://github.com/YuFy1314/YuFy1314.github.io/blob/MiccallTheme/source/images/Home_02.png?raw=true" alt="Version"></a>
</p>

## Quick start 快速开始

- 请仔细阅读 Hexo 的官方文档，完成对 Hexo 的[安装](https://hexo.io/zh-cn/docs/index.html#%E5%AE%89%E8%A3%85)和[基本的配置](https://hexo.io/zh-cn/docs/configuration.html)。

- 下载本主题并且放置于`themes`目录下，更改主题名字，并在站点根目录的配置文件`_config.yml`中启用该主题。

```
theme: miccall
```
- 在主题的配置文件`_config.yml`中修改相应的值。

## Docs 文档

以下内容均为主题的配置文件 `_config.yml`内容（请区别于站点的配置文件）。

##### 一 . head标签下 

1.网站的logo 
    **favicon:** "/img/logo.png"

2.搜索的关键字 :
keywords提供的网页关键词通常是为搜索引擎分类网页使用的；
可以为网页提供多个关键词，多个关键词应该使用空格分开；
不要给网页定义过多的关键词，最好保持在10个以下，过多的关键词，搜索引擎将忽略；
不要给网页定义与网页描述内容无关的关键词；
由于网页制作者滥用keywords(提供过多的关键词或者提供与网页无关的关键词)，导致目前常用的搜索引擎降低了keywords的重要性。
    **keywords:** yufy

3.主页背景图片：默认链接是在主站以下目录的 "img/bg.jpg" 暂不支持外链
    **backgroundpic :** "img/bg.jpg"


##### 二 . Intro: 主题刚开始加载的界面

1.名字 
    **name:** 苏日俪格

2.第二标语
    **slogan:** "Conceit makes one's progress <br/> Pride make one lag behind"

3.主页按钮上面的文字     
    **HeadButton:** 苏日俪格

##### 三 .Nav: 导航栏

```    
    Home_name: 主页 # 主页名字
    is_use_categories : true # 是否启用分类
    categories_name: 分类 # 分类名字
    is_use_archives : false # 是否启用归档
    archives_name: 归档 # 归档名字
    icon: # 导航栏上的图标
        github:
            use: true # 是否启用
            link: https://github.com/YuFy1314 # 点击地址
        user: https://yufy1314.github.io/resume/
        book: https://www.jianshu.com/u/72f239ec5d03
        Facebook:
            use: false
            link:
    pages:
    # 自定义连接页
    # link 的参数为相对路径，对应 hexo 目录下的 source 件夹内的相应文件夹
        Resume: 
            link: "/resume/"
        website:
            link: "/website/"
        #图库 :
        #    link: "/gallery/"
        #标签:
        #   link: "/tag/"
        #自定义标签名
        #   link：“路径”

    MainFirst: # 导航栏下面的主页
        name: YuFy # 大标题名字
        description: Welcome to my Blog   # 第二标签 描述
        pic_url: /img/logo.jpg # 图片地址
        goto_ulr: "https://www.jianshu.com/u/72f239ec5d03" # 点击跳转

    Gallery: # 图库页
        title: Mr.metro
        description: Just another fine responsive
```

使用方法 ：

1. 创建「resume」页面

    - 在站点根目录的`source`目录，新建一个`resume`目录，这个文件目录与 `link: "/resume/"`所对应，在里面创建一个 `index.md` 文件，在此创作 `resume`内容。

2. 创建「website」页面

    - 在站点根目录的`source`目录，新建一个`website`目录，这个文件目录与`link: "/website/"`所对应，在里面创建一个`index.md`文件。

    - 这里面的`front-matter`即为---, 可以根据hexo的官方文档来填写, [戳这里](https://hexo.io/zh-cn/docs/front-matter)

    - `front-matter`里面添加属性

        ```
        ---
        title: website
        date: 2017-01-17 21:05:04
        layout: links
        ---
        ```

    - 然后在站点根目录的 `source`目录` _data`目录(没有的话新建一个)。然后在里面新建一个`links.yml`文件，多成员依次添加。
        ```
        # 成员1
        名称 :
              link: 点击连接地址   
              avatar: 头像地址
              descr: 描述
        # 成员2
        名称 :
              link: 点击连接地址   
              avatar: 头像地址
              descr: 描述
        ```

3. 创建「gallery」页面

    - 在站点根目录的`source`目录，新建一个`galler`y目录，这个文件目录与`link: "/gallery/"`所对应 ，在里面创建一个`index.md`文件, `front-matter`里面添加属性

        ```
        ---
        title: Gallery
        date: 2017-01-17 21:39:03
        layout: gallery
        ---
        ```

    - 然后在站点根目录的`source`目录 `_data`目录(没有的话新建一个)。然后在里面新建一个`gallery.yml`文件，多图片依次添加，图片名称不要重复。

        ```
        图片名称1:
          full_link: 图片地址
          thumb_link: 略缩图地址
          descr: 图片描述
        图片名称2:
          full_link: 图片地址
          thumb_link: 略缩图地址
          descr: 图片描述
        ```

4. 创建「tag」页面


    - 在站点根目录的`source`目录，新建一个`tag`目录，这个文件目录与`link: "/tag/"`所对应  ，在里面创建一个`index.md `文件，`front-matter`里面添加属性。

        ```
        ---
        title: tags
        date: 2017-01-17 21:39:14
        layout: tags
        ---
        ```
1. 修改背景图片：更换`\themes\miccall\source\images`中的`bg.jpg`，不要改名，否则需要更改CSS内容。

2. 修改导航栏下面的个人图片：更换`\themes\miccall\source\img`中的`me.jpg`，不要改名，否则需要更改CSS内容。

3. 字体文件不建议修改。

4. 评论系统：`use`的配置选项`false | duoshuo | disqus | disqus_click | changyan`

    ```
    comment:
       use: disqus_click
       shortname: http-miccall-tech
       duoshuo_thread_key_type: path
       duoshuo_embed_js_url: "https://static.duoshuo.com/embed.js"
       changyan_appid:
       changyan_conf:
       changyan_thread_key_type: path
    ```

5. 搜索系统：

    ```
    search:
      use: google
      swiftype_key: Just another fine responsive  
    ```

6. 访问量系统

    ```
    Leancloud Views
    leancloud:
        enable: false
        app_id: # 你的 app_id
        app_key: # 你的 app_key
        av_core_mini: "https://cdn1.lncld.net/static/js/av-core-mini-0.6.1.js"
    ```


    ​```
    busuanzi:
      enable: true  #  是否开启
      all_site_uv: true # 全局启用
      post_pv: true # 单独文章启用
      busuanzi_pure_mini_js: "https://dn-lbstatics.qbox.me/busuanzi/2.3/busuanzi.pure.mini.js"
    ​```

1. 开始创作你的文章：文章目录在`blog/source/_post`目录下新建一个`.md`文件：

    ```
    ---
    title: # 文章标题  
    date: 2017/3/27 13:48:25  # 文章发表时间
    tags:
    - 标签1
    - 标签2 (可选)
    categories: Algorithm # 分类
    thumbnail: https://xxxxxxxxxx.png # 略缩图
    ---

    文章正文

    ```

### 代码高亮

安装组件参阅http://github.com/ele828/hexo-prism-plugin

#### 文中哪些不懂的地方可以参考[hexo官方文档](https://hexo.io/zh-cn/), 也可以[new issue](https://github.com/YuFy1314/YuFy1314.github.io/issues/new)
