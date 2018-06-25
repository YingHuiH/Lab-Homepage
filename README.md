



1. 文件夹下主要内容是什么？

整个网页的project文件夹下主要是几类文件：

*  放在主文件夹下的md文件（Readme.md除外）和index.html对应的是网页整个框架下的各个页面；

* _layouts 文件夹存放的是主要的网页格式模板，供主文件夹下的md/html文件套用；目前，主页用的是default.html 模板，其他页面用的是page.html 模板。

* _includes 文件夹下存放的是模板使用的各个元素。因为就网站来说，很多网站元素是可以共用的，比如导航栏、网页页脚等等。因此，在_layouts文件夹下的模板通过引用此文件夹的内容，使模板表达更为简练、使用和新建模板更为方便。

* img文件夹存放着网站需要用得到各个图片，以相对路径的方式，在各个网页中进行引用。

* assets、 js等文件夹存放的是关于格式设置等等的文件。

* _site 这个文件夹下的所有内容是自动生成的，所以不要去管它，它会自己更新。

* src\styles\main.scss 这个是网站主要样式设置文件。



2. 如何修改homepage？

index.html 是首页（即lab的homepage，星空动画），但这里我们直接让index.html套用了default模板，所以要修改homepage需要根据default模板，去修改各部分元素，例如去修改\_includes\header.html 里面的网站homepage的标题内容。



3. 如何创建一个新的子页面，并自动纳入上方的目录索引？

步骤：

* 在主文件夹下，建立一个md或者html文件（建议用md，支持在md中用html语言进行丰富的格式/样式设置）；

* 编辑新建的md或者html文件，每个md或者html的开头示例如下：

---
layout: page
title: "COURSES"
---

layout控制了使用哪个基础模板（例子中对应的是_layouts文件夹下的page模板）。而title则是控制了，这个md被索引之后的名称叫做什么。

* 按照常规的md或者html写法即可；


备注：

* 如何控制哪个子页面在前、哪个在后呢？ 网页是自动根据文件名称字母顺序来进行索引的，所以，只需要根据想要的子页面索引顺序，修改各个子页面对应的markdown/html的文件名称的首字母即可。 例如， A-people.md , B-Project.md, 则团队成员介绍网页被索引在前（A-people.md对应内容），项目介绍被索引在后（B-Project.md对应内容）。



