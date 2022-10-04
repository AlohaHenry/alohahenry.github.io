这是我的第一篇blog，写的也是如何通过github快速创建你自己的个人博客网站

最近这不到一个月有了很多改动，以前的教程都失效了，截止文章发出官方文档也是错误的，反反复复排查，发现根本不是我的操作问题

![image-20221004下午65737718](/Users/alohahenry/Library/Application Support/typora-user-images/image-20221004下午65737718.png)

首先打开github.com

![image-20221004下午63601653](/Users/alohahenry/Library/Application Support/typora-user-images/image-20221004下午63601653.png)

点击Your profile

![image-20221004下午63749250](/Users/alohahenry/Library/Application Support/typora-user-images/image-20221004下午63749250.png)

创建新的repository

![image-20221004下午63932770](/Users/alohahenry/Library/Application Support/typora-user-images/image-20221004下午63932770.png)

**注意：名字必须输入为格式： 用户名.github.io**

我填写alohahenry.github.io

![image-20221004下午64134536](/Users/alohahenry/Library/Application Support/typora-user-images/image-20221004下午64134536.png)

（我创建了同名文件所以点击不了）

![image-20221004下午64323860](/Users/alohahenry/Library/Application Support/typora-user-images/image-20221004下午64323860.png)

一开始应该是没有我的config文件的

![image-20221004下午64428194](/Users/alohahenry/Library/Application Support/typora-user-images/image-20221004下午64428194.png)

所有都可以用默认设置，但很多教程包括官方文档告诉你到了这里应该点击“Chooser a Theme”，但是**根本没有这个按钮，并且实际上就是什么都不会有**

![image-20221004下午64702748](/Users/alohahenry/Library/Application Support/typora-user-images/image-20221004下午64702748.png)

所以返回并添加新文件，**命名：_config.yml**

![image-20221004下午64828047](/Users/alohahenry/Library/Application Support/typora-user-images/image-20221004下午64828047.png)

并在内容处填写（可以替换为其他主题）

```yaml
remote_theme: vszhub/not-pure-poole
plugins:  
  - jekyll-remote-theme
```

![image-20221004下午65310904](/Users/alohahenry/Library/Application Support/typora-user-images/image-20221004下午65310904.png)

至此，等待2~3分钟后访问**用户名.github.io**，如果成功，恭喜

![image-20221004下午70031180](/Users/alohahenry/Library/Application Support/typora-user-images/image-20221004下午70031180.png)

以后所有配置文件都是不自带的，但是github应该是能读取，如果有了解欢迎告诉我，我也是小白，沟通或汇报问题发邮件至*aloha.henry.2018@gmail.com*随时联系