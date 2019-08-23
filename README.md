

![](https://raw.githubusercontent.com/qiubaiying/qiubaiying.github.io/master/img/readme-home.png)

[![Build Status](https://travis-ci.org/qiubaiying/qiubaiying.github.io.svg?branch=master)](https://travis-ci.org/qiubaiying/qiubaiying.github.io)
[![codebeat badge](https://codebeat.co/badges/5f031df3-f6c1-4ec0-911a-ff6617ca50b9)](https://codebeat.co/projects/github-com-qiubaiying-qiubaiying-github-io-master)
[![GitHub issues](https://img.shields.io/github/issues/qiubaiying/qiubaiying.github.io.svg?style=flat)](https://github.com/qiubaiying/qiubaiying.github.io/issues)
[![License MIT](https://img.shields.io/badge/license-MIT-blue.svg?style=flat)](https://github.com/home-assistant/home-assistant-iOS/blob/master/LICENSE)
[![](https://img.shields.io/github/stars/qiubaiying/qiubaiying.github.io.svg?style=social&label=Star)](https://github.com/qiubaiying/qiubaiying.github.io)
[![](https://img.shields.io/github/forks/qiubaiying/qiubaiying.github.io.svg?style=social&label=Fork)](https://github.com/qiubaiying/qiubaiying.github.io)


博客的搭建教程修改自 [Hux](https://github.com/Huxpro/huxpro.github.io)

更为详细的教程戳这 [《利用 GitHub Pages 快速搭建个人博客》](http://www.jianshu.com/p/e68fba58f75c) 或 [wiki](https://github.com/qiubaiying/qiubaiying.github.io/wiki/%E5%8D%9A%E5%AE%A2%E6%90%AD%E5%BB%BA%E8%AF%A6%E7%BB%86%E6%95%99%E7%A8%8B)

>
### [查看博客戳这里 👆](http://qiubaiying.github.io)



## 使用

* 开始
	* [环境](#环境)
	* [开始](#开始)
	* [撰写博文](#撰写博文)
* 组件
	* [侧边栏](#侧边栏)
	* [迷你关于我](#mini-about-me)
	* [推荐标签](#featured-tags)
	* [好友链接](#friends)
	* [HTML5 演示文档布局](#keynote-layout)
* 评论与 Google/Baidu Analytics
	* [评论](#comment)
	* [网站分析](#analytics)
* 高级部分
	* [自定义](#customization)
	* [标题底图](#header-image)
	* [搜索展示标题-头文件](#seo-title)



### 环境

如果你安装了 [jekyll](http://jekyllcn.com/)，那你只需要在命令行输入`jekyll serve` 或 `jekyll s`就能在本地浏览器中输入`http://127.0.0.1:4000/`预览主题，对主题的修改也能实时展示（需要强刷浏览器）。



### 开始

你可以通用修改 `_config.yml`文件来轻松的开始搭建自己的博客:

```
# Site settings
title: BY Blog                    # 你的博客网站标题
SEOTitle: 柏荧的博客 | BY Blog		# SEO 标题
description: "Hey"	   	   # 随便说点，描述一下

# SNS settings      
github_username: qiubaiying     # 你的github账号
jianshu_username: e71990ada2fd  # 你的简书ID。

# Build settings
# paginate: 10              # 一页你准备放几篇文章
```

Jekyll官方网站还有很多的参数可以调，比如设置文章的链接形式...网址在这里：[Jekyll - Official Site](http://jekyllrb.com/) 中文版的在这里：[Jekyll中文](http://jekyllcn.com/).

### 撰写博文

要发表的文章一般以 **Markdown** 的格式放在这里`_posts/`，你只要看看这篇模板里的文章你就立刻明白该如何设置。

yaml 头文件长这样:

```
---
layout:     post
title:      定时器 你真的会使用吗？
subtitle:   iOS定时器详解
date:       2016-12-13
author:     BY
header-img: img/post-bg-ios9-web.jpg
catalog: 	 true
tags:
    - iOS
    - 定时器
---

```

### 侧边栏

看右边:
![](https://raw.githubusercontent.com/qiubaiying/qiubaiying.github.io/master/img/readme-side.png)

设置是在 `_config.yml`文件里面的`Sidebar settings`那块。

```
# Sidebar settings
sidebar: true  #添加侧边栏
sidebar-about-description: "简单的描述一下你自己"
sidebar-avatar: /img/avatar-by.jpg     #你的大头贴，请使用绝对地址.注意：名字区分大小写！后缀名也是
```

侧边栏是响应式布局的，当屏幕尺寸小于992px的时候，侧边栏就会移动到底部。具体请见bootstrap栅格系统 <http://v3.bootcss.com/css/>


### Mini About Me

Mini-About-Me 这个模块将在你的头像下面，展示你所有的社交账号。这个也是响应式布局，当屏幕变小时候，会将其移动到页面底部，只不过会稍微有点小变化，具体请看代码。

### Featured Tags

看到这个网站 [Medium](http://medium.com) 的推荐标签非常的炫酷，所以我将他加了进来。
这个模块现在是独立的，可以呈现在所有页面，包括主页和发表的每一篇文章标题的头上。

```
# Featured Tags
featured-tags: true  
featured-condition-size: 1     # A tag will be featured if the size of it is more than this condition value
```

唯一需要注意的是`featured-condition-size`: 如果一个标签的 SIZE，也就是使用该标签的文章数大于上面设定的条件值，这个标签就会在首页上被推荐。

内部有一个条件模板 `{% if tag[1].size > {{site.featured-condition-size}} %}` 是用来做筛选过滤的.

### Social-media Account

在下面输入的社交账号，没有的添加的不会显示在侧边框中。新加入了[简书](https:/www.jianshu.com)链接, <http://www.jianshu.com/u/e71990ada2fd>

	# SNS settings
	RSS: false
	jianshu_username: 	jianshu_id
	zhihu_username:     username
	facebook_username:  username
	github_username:    username
	# weibo_username:   username



![](http://ww4.sinaimg.cn/large/006tKfTcgy1fgrgbgf77aj308i02v748.jpg)

### Friends

好友链接部分。这会在全部页面显示。

设置是在 `_config.yml`文件里面的`Friends`那块，自己加吧。

```
# Friends
friends: [
    {
        title: "BY Blog",
        href: "https://qiubaiying.github.io/"
    },
    {
        title: "Apple",
        href: "https://apple.com/"
    }
]
```


### Keynote Layout

HTML5幻灯片的排版：

![](https://camo.githubusercontent.com/f30347a118171820b46befdf77e7b7c53a5641a9/687474703a2f2f6875616e677875616e2e6d652f696d672f626c6f672d6b65796e6f74652e6a7067)

这部分是用于占用html格式的幻灯片的，一般用到的是 Reveal.js, Impress.js, Slides, Prezi 等等.我认为一个现代化的博客怎么能少了放html幻灯的功能呢~

其主要原理是添加一个 `iframe`，在里面加入外部链接。你可以直接写到头文件里面去，详情请见下面的yaml头文件的写法。

```
---
layout:     keynote
iframe:     "http://huangxuan.me/js-module-7day/"
---
```

iframe在不同的设备中，将会自动的调整大小。保留内边距是为了让手机用户可以向下滑动，以及添加更多的内容。


### Comment

博客不仅支持 [Disqus](http://disqus.com) 评论系统,还加入了 [Gitalk](https://gitalk.github.io/) 评论系统，[支持 Markdwon 语法](https://guides.github.com/features/mastering-markdown/)，cool~

#### Disqus

优点：国际比较流行，界面也很大气、简洁，如果有人评论，还能实时通知，直接回复通知的邮件就行了；

缺点：评论必须要去注册一个disqus账号，分享一般只有Facebook和Twitter，另外在墙内加载速度略慢了一点。想要知道长啥样，可以看以前的版本点[这里](http://brucezhaor.github.io/about.html) 最下面就可以看到。

> Node：有很多人反映 Disqus 插件加载不出来，可能墙又架高了，有条件的话翻个墙就好了~

**使用：**

**首先**，你需要去注册一个Disqus帐号。**不要直接使用我的啊！**

**其次**，你只需要在下面的 yaml 头文件中设置一下就可以了。

```
# 评论系统
# Disqus（https://disqus.com/）
disqus_username: qiubaiying
```

#### Gitalk

优点：界面干净简洁，利用 Github issue API 做的评论插件，使用 Github 帐号进行登录和评论，最喜欢的支持 Markdown 语法，对于程序员来说真是太 cool 了。

缺点：配置比较繁琐，每篇文章的评论都需要初始化。

**使用：**

参考我的这篇文章：[《为博客添加 Gitalk 评论插件》](http://qiubaiying.top/2017/12/19/%E4%B8%BA%E5%8D%9A%E5%AE%A2%E6%B7%BB%E5%8A%A0-Gitalk-%E8%AF%84%E8%AE%BA%E6%8F%92%E4%BB%B6/)


### Analytics

网站分析，现在支持百度统计和Google Analytics。需要去官方网站注册一下，然后将返回的code贴在下面：

```
# Baidu Analytics
ba_track_id: 4cc1f2d8f3067386cc5cdb626a202900

# Google Analytics
ga_track_id: 'UA-49627206-1'            # 你用Google账号去注册一个就会给你一个这样的id
ga_domain: huangxuan.me			# 默认的是 auto, 这里我是自定义了的域名，你如果没有自己的域名，需要改成auto。
```

### Customization

如果你喜欢折腾，你可以去自定义这个模板的 Code。

**如果你可以理解 `_include/` 和 `_layouts/`文件夹下的代码（这里是整个界面布局的地方），你就可以使用 Jekyll 使用的模版引擎 [Liquid](https://github.com/Shopify/liquid/wiki)的语法直接修改/添加代码，来进行更有创意的自定义界面啦！**

### Header Image

博客每页的标题底图是可以自己选的，看看几篇示例post你就知道如何设置了。

标题底图的选取完全是看个人的审美了。每一篇文章可以有不同的底图，你想放什么就放什么，最后宽度要够，大小不要太大，否则加载慢啊。

> 上传的图片最好先压缩，这里推荐 imageOptim 图片压缩软件，让你的博客起飞。

但是需要注意的是本模板的标题是**白色**的，所以背景色要设置为**灰色**或者**黑色**，总之深色系就对了。当然你还可以自定义修改字体颜色，总之，用github pages就是可以完全的个性定制自己的博客。

### SEO Title

我的博客标题是 **“BY Blog”** 但是我想要在搜索的时候显示 **“柏荧的博客 | BY Blog”** ，这个就需要 SEO Title 来定义了。

其实这个 SEO Title 就是定义了<head><title>标题</title></head>这个里面的东西和多说分享的标题，你可以自行修改的。

### 关于收到"Page Build Warning"的 Email

由于jekyll升级到3.0.x,对原来的 pygments 代码高亮不再支持，现只支持一种-rouge，所以你需要在 `_config.yml`文件中修改为 `highlighter: rouge` .另外还需要在`_config.yml`文件中加上`gems: [jekyll-paginate]`.

同时,你需要更新你的本地 jekyll 环境.

使用`jekyll server`的同学需要这样：

1. `gem update jekyll` # 更新jekyll
2. `gem update github-pages` #更新依赖的包

使用`bundle exec jekyll server`的同学在更新 jekyll 后，需要输入`bundle update`来更新依赖的包.

> Note：
> 可以使用 `jekyll -s` 命令在本地实时配置博客，提高效率。详见 [Jekyll.com](http://jekyllcn.com/)

参考文档：[using jekyll with pages](https://help.github.com/articles/using-jekyll-with-pages/) & [Upgrading from 2.x to 3.x](http://jekyllrb.com/docs/upgrading/2-to-3/)



Jekyll Compose
安装了 Jekyll Compose 后，Jekyll 会额外提供一些命令，便于发布管理博文。

安装
将此行添加到应用程序的Gemfile：

gem 'jekyll-compose', group: [:jekyll_plugins]
然后执行：

$ bundle
用法
安装完成后（见上文），运行后你会bundle exec jekyll help看到：

在帮助中列出，您将看到可用的新命令：

  草案       ＃创建指定名称的新岗位草案
  后        ＃创建一个新的职位给定名称
  发布     ＃移动一个选秀进入_posts目录，并设置日期
  取消发布   ＃移动后回_drafts目录
  页        ＃创建一个新的页面与给定的NAME
使用以下方式创建新页面：

$ jekyll page "My New Page"
使用以下内容创建新帖子：

$ jekyll post "My New Post"
使用以下方法创建新草稿：

$ jekyll draft "My new draft"
使用以下内容发布草稿：

$ jekyll publish _drafts/my-new-draft.md

# or specify a specific date on which to publish it
$ bundle exec jekyll publish _drafts/my-new-draft.md --date 2014-01-24
使用以下内容取消发布您的帖子：

$ bundle exec jekyll unpublish _posts/2014-01-24-my-new-draft.md
组态
要自定义默认插件配置，请编辑jekyll_composejekyll配置文件中的部分。

在编辑器中自动打开新的草稿或帖子
  jekyll_compose：
     auto_open：true
并确保您有EDITOR或JEKYLL_EDITOR环境变量设置。例如，如果您希望在Atom编辑器中打开新创建的Jekyll帖子和草稿，则可以在shell配置中添加以下行：

export JEKYLL_EDITOR=atom
后者将覆盖默认EDITOR值。

设置草稿和帖子的默认前端内容
如果您希望将默认前置事项添加到新创建的帖子或草稿中，您可以根据需要指定任意数量draft_default_front_matter和post_default_front_matter配置键，例如：

jekyll_compose：
   draft_default_front_matter：
     description：
     image：
     category：
     tags：
   post_default_front_matter：
     description：
     image：
     category：
     tags：
     published：false
    sitemap：false
这也将自动添加：

dateattribure 下的创建时间戳。
属性下的title title属性

Jekyll SEO Tag
Jekyll SEO Tag 帮你生成一大堆 Meta 标签。
Jemoji
你可以通过 Jemoji 在 Jekyll 生成的网站中，加入自己 Emoji 表情。
Emoji 语法采用 GitHub 的语法风格。
Jekyll Mentions
Jekyll Mentions 允许你在文章中直接“@” GitHub 或其它网站用户。
Jekyll Feed
你可以通过 Jekyll Feed 在 Jekyll 生成的网站中，生成 RSS 源。
Jekyll Import
Jekyll Import 支持从一些国外的主流站点导入博文，如 Blogger, WordPress 和 Tumblr 等，同样也支持 RSS 和 CSV 等数据格式导入。
Jekyll Archives
Jekyll Archives 用于生成带标签和分类的『存档』页面。
Jekyll Redirect From
Jekyll Redirect From 提供页面跳转功能，比较简单，也可以自行通过 JavaScript 实现

五、使用Markdown
5.1 简介
Markdown 的宗旨是实现「易读易写」。可读性，无论如何，都是最重要的。

Markdown 的语法全由一些符号所组成，这些符号经过精挑细选，其作用一目了然。格式撰写的文件可以直接以纯文本发布，并且看起来不会像是由许多标签或是格式指令所构成。

资料：

http://www.cnblogs.com/purediy/archive/2013/01/10/2855397.html
5.2 基本语法
1、使用一个或多个空行分隔内容段来生成段落 <p>。

2、标题（h1~h6）格式为使用相应个数的“#”作前缀。

比如以下代码表示 h3：
### this is a level-3 header ###
3、使用“>”作为段落前缀来标识引用文字段落。这其实是 email 中标记引用文字的标准方式：

> 引用的内容
> 这个记号直接借鉴的邮件标准
4、使用“*”“+”“-”来表示无序列表；使用数字加“.”表示有序列表。如：

1. I am ordered list item 1...
2. So I should be item 2!?
5、使用 4 个以上 空格或 1 个以上 的 tab 来标记代码段落，它们将被<pre> 和 <code> 包裹，这意味着代码段内的字体会是 monospace家族的，并且特殊符号不会被转义。

6、使用 [test](http://example.net "optional title") 来标记普通链接。

7、使用 ![img](http://example.net/img.png "optional title") 来标记图片。

引号内的 title 文字是可选的，链接也可以使用相对路径。
8、使用 * 或 _ 包裹文本产生 strong 效果：

_语气很重的文本_ 以及 **语气更重的文本**

同时我再介绍一些Markdown语法
首先是最重要的换行，在段落内换行时，单纯的回车换行是不行的，必须在每行末尾处增加至少两个空格才能实现换行。

如果想实现两段文字中产生分段的效果，只要在两行文字中空一行即可实现。
接着是和本段文字类似的列表，在列表每项前增加”-“、”+”或”*“再接三个空格即可。

如果需要带数字的列表，则可以使用’1.’接一个空格来创建。

如果需要输入代码，那么可以在代码首尾两行用四个空格或```包围即可，使用```包围代码时，可以在首行的```后指定代码格式进行高亮，比如```java，但是代码能不能高亮要看markdown支持的实际情况。

如果要输入一段引用内容，可以使用’>’再接文字，比如下面这段就是>测试文本输入的。
测试文本

关于插入图片，我这里用Github仓库来存图片，文章内的图片使用了绝对地址来引用，步骤如下：

将图片放在仓库内的assets\images\2018\use-github-pages目录下。
在文章内插入图片链接，格式为http://mcace.me/assets/images/2018/use-github-pages/图片名

九、编辑、发布文章
现在我们已经有一套博客了，下面就是最重要的写文章部分了，在markdown文本编辑环境中我选择了Sublime Text 3+Markdown Editing插件，Sublime Text 3是一款免费的本文编辑器，支持安装多种插件，我也用过同类型的Notepad++，但始终觉得Sublime Text界面更加友好，插件更易用。

安装Markdown Editing插件
首先Sublime Text 3在安装插件之前，要安装Package Control插件，这个插件可以用于安装各种Sublime Text的插件。

打开Sublime Text 3，按Ctrl+`呼出控制台，输入下面这行命令后回车:

import urllib.request,os,hashlib; h = ‘6f4c264a24d933ce70df5dedcf1dcaee’ + ‘ebe013ee18cced0ef93d5f746d80ef60’; pf = ‘Package Control.sublime-package’; ipp = sublime.installed_packages_path(); urllib.request.install_opener( urllib.request.build_opener( urllib.request.ProxyHandler()) ); by = urllib.request.urlopen( ‘http://packagecontrol.io/’ + pf.replace(‘ ‘, ‘%20’)).read(); dh = hashlib.sha256(by).hexdigest(); print(‘Error validating download (got %s instead of %s), please try manual install’ % (dh, h)) if dh != h else open(os.path.join( ipp, pf), ‘wb’ ).write(by)

稍等片刻，控制台会给出一串数字，这时重启Sublime Text 3即可。

重启后按Ctrl+Shift+P打开包管理界面，在文本框中输入”pcip”，如果Package Controller被正确安装则会显示”Package Control： Install Package”，这时按下回车即可进入包安装界面（可能要稍微等一会才弹出），输入”Markdown Editing”即可找到插件，按回车即可进行安装。

但不知什么原因，我的Package Control找不到Markdown Editing，因此这里再介绍另一种安装Sublime Text插件的方法： 首先在这里下载Markdown Editing的官方打包。

下载完成后用“解压到当前文件夹”进行解压缩，然后将”MarkdownEditing-master”文件夹改名为”MarkdownEditing”，再移动到Sublime Text 3的插件目录下，插件目录可以通过在Sublime Text 3下按Alt+N -> B来找到。

这时重启Sublime Text 3，按Ctrl+Shift+P打开包管理界面，输入”Markdown Editing”即可找到该插件。

## 致谢

1. 这个模板是从这里 [Hux](https://github.com/Huxpro/huxpro.github.io) fork 的, 感谢这个作者。
2. 感谢 Jekyll、Github Pages 和 Bootstrap!

## License

遵循 MIT 许可证。有关详细,请参阅 [LICENSE](https://github.com/qiubaiying/qiubaiying.github.io/blob/master/LICENSE)。
