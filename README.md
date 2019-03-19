白卷是一个前后端分离的图书管理系统，项目采用 SpringBoot+Vue 开发。  


项目地址：[https://github.com/Antabot/White-Jotter](https://github.com/Antabot/White-Jotter)       

# 前言 

这是一个简单的小项目，旨在熟悉 Java Web 项目开发流程，我会把开发的经验分享给大家，包括需求分析、网页设计、原型、功能实现等，并尽量采用目前较为流行的技术。

由于 Web 开发只是我的个人兴趣而非职业，难免有许多不足之处，希望路过的大神们能够帮忙指出。

# 一、整体效果

## 1.首页

作为展示页面，包括开发这个项目的主要参考资料和 Slogan

![](https://img-blog.csdnimg.cn/20190319170913120.png)

## 2.图书馆

作为核心功能页面之一，提供图书信息展示、图书信息管理两大功能

![](https://img-blog.csdnimg.cn/20190319170929209.png)

## 3.笔记本

该页面尚未成型

# 二、技术栈

## 1.前端技术栈

1.Vue  
2.ElementUI  
3.axios   

## 2.后端技术栈

1.SpringBoot  
2.SpringSecurity  
3.MySQL  
  
在开发过程中还会不断用到一些细碎的技术，有必要的我会增添上去

# 三、部署方法

1.clone项目到本地`git@github.com:Antabot/White-Jotter.git`

2.数据库脚本放在 `wj` 项目的 `resources` 目录下，在MySQL中执行数据库脚本  

3.数据库配置在 `wj` 项目的 `resources` 目录下的`application.properties` 文件中  

4.在IntelliJ IDEA中运行 `wj` 项目  

至此，服务端就启动成功了，此时在地址栏输入 `http://localhost:8443` 即可访问项目登录页面，默认账号为 `admin`，密码为 `123`

如果要做二次开发，请继续看第五、六步。

5.进入到 `wj-vue` 目录中，在命令行依次输入如下命令：  

```
# 安装依赖
npm install

# 在 localhost:8080 启动项目
npm run dev
```  

由于在 `wj-vue` 项目中已经配置了端口转发，将数据转发到SpringBoot上，因此项目启动之后，在浏览器中输入 `http://localhost:8080` 就可以访问我们的前端项目了，所有的请求通过端口转发将数据传到 SpringBoot 中（注意此时不要关闭 SpringBoot 项目）。

6.最后可以用 `WebStorm` 等工具打开 `wj-vue`项目，继续开发，开发完成后，当项目要上线时，依然进入到 `wj-vue` 目录，然后执行如下命令：  

```
npm run build
```  

该命令执行成功之后， `wj-vue` 目录下生成一个 `dist` 文件夹，将该文件夹中的两个文件 `static` 和 `index.html` 拷贝到 SpringBoot 项目中 `resources/static/` 目录下，然后就可以像第 4 步那样直接访问了。  


# 文档

文档包括项目的需求分析以及对项目开发过程中遇到的一些问题的详细记录，主要是为了帮助小伙伴们快速理解这个项目。  

1.[需求文档]()  


# 更新记录


# 其他资料

 

 