```text
---
layout: post
title: macos用jekyll创建github blog
---
```

这是我的第一篇blog，写的也是如何通过github快速创建你自己的个人博客网站

最近8月有了些改动，截止文章发出官方文档也是错误的，整完后才发现根本不是我的操作问题

首先打开github.com

![1](https://github.com/AlohaHenry/alohahenry.github.io/blob/main/_images/2022-10-4-macos用jekyll创建github个人博客/image-20221004%E4%B8%8B%E5%8D%8863601653.png?raw=true)

![image-20221004下午63749250](https://github.com/AlohaHenry/alohahenry.github.io/blob/main/_images/image-20221004%E4%B8%8B%E5%8D%8863749250.png?raw=true)

![image-20221004下午63932770](https://github.com/AlohaHenry/alohahenry.github.io/blob/main/_images/2022-10-4-macos用jekyll创建github个人博客/image-20221004%E4%B8%8B%E5%8D%8863932770.png?raw=true)

**注意：名字必须输入为格式： 用户名.github.io**

我填写alohahenry.github.io

![image-20221004下午64134536](https://github.com/AlohaHenry/alohahenry.github.io/blob/main/_images/2022-10-4-macos用jekyll创建github个人博客/image-20221004%E4%B8%8B%E5%8D%8864134536.png?raw=true)

（我创建了同名文件所以点击不了）![image-20221004下午64428194](https://github.com/AlohaHenry/alohahenry.github.io/blob/main/_images/2022-10-4-macos用jekyll创建github个人博客/image-20221004%E4%B8%8B%E5%8D%8864428194.png?raw=true)

所有都可以用默认设置，但很多教程包括官方文档告诉你到了这里应该点击“Chooser a Theme”，但是**根本没有这个按钮，并且实际上就是什么都不会有**

![image-20221004下午65737718](https://github.com/AlohaHenry/alohahenry.github.io/blob/main/_images/2022-10-4-macos%E7%94%A8jekyll%E5%88%9B%E5%BB%BAgithub%E4%B8%AA%E4%BA%BA%E5%8D%9A%E5%AE%A2/image-20221004%E4%B8%8B%E5%8D%8865737718.png?raw=true)

这是原因，所以先想着用默认主题吧，后面有了文件改着就简单，但弃用主题选择器意味着不得不碰一点命令行

**接下来没图所以一行一行读仔细了**

这时我开始翻官方文档了：

我先下载了github desktop

![a](https://github.com/AlohaHenry/alohahenry.github.io/blob/main/_images/2022-10-4-macos用jekyll创建github个人博客/Snipaste_2022-10-05_09-56-58.png?raw=true)

然后按照提示正常登入我的 GitHub 账号，然后 Clone 下来那个 GitHub Pages 项目

切到命令行，切到用户的Documents/Github/**用户名**.github.io目录下

输入：（得装homebrew

`brew install chruby ruby-install git`

`ruby-install ruby`

可能会出现一些报错像libffi libyaml没安装，也用`brew install xxx`安装了就行

再输入`gem install bundler`

结果从这里这个bundler一直没装上

我的解决方案是（卸了重装ffi）

```text
sudo gem uninstall ffi <-没有sudo可能提示没有权限
sudo bundle config build.ffi --enable-libffi-alloc
sudo gem install ffi -- --enable-libffi-alloc
bundle init
bundle install
jekyll new . --force <-此处必须有--force 也不能起名字否则另开目录
```

至此，你会发现Github Desktop多了一堆文件，Fetch上去之后大功告成，再改主题进入xxx.github.io/_config.yml按照主题所在github项目下的改动和说明就可以改主题，然后写文章就看\_posts文件夹的说明文件，应该就可以运作了

如果出现问题可以给aloha.henry.2018@gmail.com发邮件，我会及时回复或修正文章的

如果能帮到就太好了，当时整了一堆错误，不过发出来也证明完好了！

