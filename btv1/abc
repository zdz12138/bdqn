#!/bin/bash
#这是一个随便写的脚本
Shell脚本介绍
1、Shell脚本,就是利用Shell的命令解释的功能，对一个纯文本的文件进行解析，然后执行这些功能，也可以说Shell脚本就是一系列命令的集合。
2、Shell可以直接使用在win/Unix/Linux上面，并且可以调用大量系统内部的功能来解释执行程序，如果熟练掌握Shell脚本，可以让我们操作计算机变得更加轻松，也会节省很多时间。
3、Shell是一种脚本语言，那么，就必须有解释器来执行这些脚本，常见的脚本解释器有：
（1）、bash：是Linux标准默认的shell。bash由Brian Fox和Chet Ramey共同完成，是BourneAgain Shell的缩写，内部命令一共有40个。
（2）、sh： 由Steve Bourne开发，是Bourne Shell的缩写，sh 是Unix 标准默认的shell。
另外还有：ash、 csh、 ksh等。

常见的编程语言分为两类：一个是编译型语言，如：c/c++/java等，它们远行前全部一起要经过编译器的编译。另一个解释型语言，执行时，需要使用解释器一行一行地转换为代码，如：awk, perl, python与shell等。

4、使用场景，能做什么
（1）、将一些复杂的命令简单化(平时我们提交一次github代码可能需要很多步骤，但是可以用Shell简化成一步)
（2）、可以写一些脚本自动实现一个工程中自动更换最新的sdk(库)
（3）、自动打包、编译、发布等功能
（4）、清理磁盘中空文件夹
总之一切有规律的活脚本都可以尝试一下

编写一个简单的shell脚本
#!/bin/bash
# 上面中的 #! 是一种约定标记, 它可以告诉系统这个脚本需要什么样的解释器来执行;
echo "Hello, world!”
将以上内容保存在一个.sh格式的文件中，执行以下命令
bash test1.sh 或者 . test1.sh
最后输出 Hello, world!

创建一个shell脚本 ，通过shell脚本当前目录创建一个test文件夹，复制test1.sh文件到test文件夹里，进入文件夹test初始化一个npm并按照一个npm模块，通过执行 bash test2.sh命令
#!/bin/bash
# 上面中的 #! 是一种约定标记, 它可以告诉系统这个脚本需要什么样的解释器来执行;

echo "test2.sh start..."
mkdir test
cp -rf test1.sh test/
cd test
npm init
npm i --save lodash
echo "test2.sh end..."
写成一行，使用&&符号连接
mkdir test && cp -rf test1.sh test/  && cd test && npm init && npm i --save lodash
行尾使用反斜杠\使其能接着输入其他命令，不马上执行命令
echo "test2.sh start..."
mkdir test && \
    cp -rf test1.sh test/ && \
    cd test && \
    npm init && \
    npm i --save lodash
echo "test2.sh end..."
行尾添加反斜杠 ,作用是不马上执行命令可接着输入其他命令，如下

[yd@bogon:~/Documents/www/workspa/test/shell]$ mkdir test2 && \
> cd test2 && \
> npm init && \
> npm install loadsh --save
shell脚本参数传递，通过$0，$1，$2可以接收命令行传递的参数，$0 就是你写的shell脚本本身的名字，$1 是你给你写的shell脚本传的第一个参数，$2 是你给你写的shell脚本传的第二个参数
复制以下内容到test2.sh文件中

echo "shell脚本本身的名字: $0"
echo "传给shell的第一个参数: $1"
echo "传给shell的第二个参数: $2”
然后 执行命令bash test2.sh 1 2，可以看到输出结果
shell脚本本身的名字: test2.sh
传给shell的第一个参数: 1
传给shell的第二个参数: 2

编写一个自动提交git的shell脚本
创建gitautopush.sh文件，将以下内容复制进去

#!/bin/bash
# 上面中的 #! 是一种约定标记, 它可以告诉系统这个脚本需要什么样的解释器来执行;

echo "gitautopush start..."
git add .
git commit -m $1
echo "git提交注释:$1"
git push origin master
echo "gitautopush end..."
以上自动提交git脚本就写好了，现在输入以下命令执行脚本
bash gitautopush.sh 自动提交测试

控制台输出 ，代码已经成功提交到git服务器了

gitautopush start...
[master be8d56b] shell
 3 files changed, 51 insertions(+)
 create mode 100644 shelldemo/gitautopush.sh
 create mode 100644 shelldemo/test1.sh
 create mode 100644 shelldemo/test2.sh
git提交注释:自动提交测试
Counting objects: 6, done.
Delta compression using up to 4 threads.
Compressing objects: 100% (6/6), done.
Writing objects: 100% (6/6), 1.14 KiB | 1.14 MiB/s, done.
Total 6 (delta 2), reused 0 (delta 0)
remote: Resolving deltas: 100% (2/2), completed with 1 local object.
To https://github.com/fozero/frontcode.git
   2e79d26..be8d56b  master -> master
gitautopush end...
参考
https://www.cnblogs.com/gaosheng-221/p/6794429.html
https://www.cnblogs.com/yinheyi/p/6648242.html

作者：fozero
文章出处：https://www.cnblogs.com/fozero
声明：本文版权归作者和博客园共有，欢迎转载，但未经作者同意必须保留此段声明，且在文章页面明显位置给出原文连接，否则保留追究法律责任的权利。
分类: shell
标签: shell
好文要顶 关注我 收藏该文
fozero
关注 - 15
粉丝 - 39
+加关注
1 0
« 上一篇：一篇迟到的gulp文章，代码合并压缩，less编译
» 下一篇：mac使用brew安装mysql
posted @ 2018-06-04 17:34 fozero 阅读(1369) 评论(0) 编辑 收藏
刷新评论刷新页面返回顶部
注册用户登录后才能发表评论，请 登录 或 注册，访问网站首页。
相关博文：
· 360加固的自动化处理脚本
· shell 脚本 自动化
· 解放双手——Android自动化测试
· 使用dbstart 和dbshut 脚本来自动化启动和关闭数据库
· dos脚本批量文件重命名，自动化处理
热门推荐：
· 我去暗网里转了转（慎入）
· “暗网”真的如传言般可怕吗？这是一份《暗网指南》
· 如何进入暗网（技术交流）
· Node.js安装及环境配置
· 深网与暗网初学者指南
公告
昵称：fozero
园龄：2年11个月
粉丝：39
关注：15
+加关注
<	2018年12月	>
日	一	二	三	四	五	六
25	26	27	28	29	30	1
2	3	4	5	6	7	8
9	10	11	12	13	14	15
16	17	18	19	20	21	22
23	24	25	26	27	28	29
30	31	1	2	3	4	5
搜索




常用链接
我的随笔
我的评论
我的参与
最新评论
我的标签
最新随笔
1. koa2入门使用总结
2. git在工作中的用法总结-使用篇
3. git在工作中的用法总结-环境安装篇
4. 升级mac Mojave系统,git无法使用
5. checkbox在vue中的用法总结
6. 基于vue2.0实现仿百度前端分页效果（二）
7. 基于vue2.0实现仿百度前端分页效果（一）
8. mac使用brew安装mysql
9. 使用shell脚本来自动化处理我们的工作，解放双手
10. 一篇迟到的gulp文章，代码合并压缩，less编译
我的标签
前端(60)
js(30)
css(18)
vuejs(9)
个人总结(7)
微信小程序(5)
git(5)
html(4)
问题解决(4)
跨平台(4)
更多
随笔分类(166)
Android(5)
ES5/ES6(2)
Git(4)
Gulp/Webpack(2)
Hadoop
HTML5/CSS3(19)
Http/Https协议(3)
iOS(2)
Java(2)
JS/JQUERY(33)
Less/Sass(1)
Maven(3)
MongoDB
MyBatis(2)
Mysql(2)
Nodejs(2)
Oracle
Python之旅(1)
React Native从入门到"放弃"系列(2)
React/React Native(2)
shell(1)
Spring(1)
Vuejs(12)
Weex(2)
百度地图(2)
电脑技巧(4)
高德地图(1)
个人总结(13)
开发工具(8)
开发资源
面试技巧(4)
设计模式
微信小程序(5)
性能优化(2)
转载(24)
随笔档案(137)
2018年12月 (4)
2018年11月 (1)
2018年10月 (3)
2018年6月 (1)
2018年5月 (1)
2018年4月 (5)
2018年3月 (5)
2018年2月 (3)
2018年1月 (4)
2017年12月 (4)
2017年11月 (10)
2017年9月 (2)
2017年8月 (1)
2017年7月 (2)
2017年6月 (29)
2017年5月 (2)
2017年4月 (2)
2017年3月 (4)
2017年2月 (5)
2017年1月 (1)
2016年12月 (23)
2016年11月 (6)
2016年10月 (5)
2016年9月 (9)
2016年8月 (4)
2016年3月 (1)
积分与排名
积分 -	139489
排名 -	2658
最新评论
1. Re:git在工作中的用法总结-使用篇
学习了，原来还可以在COMMIT的时候，添加表情.
git ci -m ':bug: fix click of get with no feedback'
--好好长大
2. Re:使用IntelliJ IDEA和Maven构建Java web项目并打包部署
那我岂不是没改一次就要打包复制一次，这不得疯啊
--毕业那天如果没有告别？
3. Re:使用IntelliJ IDEA和Maven构建Java web项目并打包部署
大哥，虽然这个是可行的，但是也太麻烦了吧。有没有简单快速一点的啊！就像eclipse里面一样
--毕业那天如果没有告别？
4. Re:微信小程序中this指向作用域问题this.setData is not a function报错
这篇内容帮到了我，赞一个。
--mier红岩
5. Re:史上最全常用正则表达式大全
为啥没有银行卡号？
--春至燕归来
阅读排行榜
1. JS中将一个值转换为字符串的3种方法(124679)
2. 史上最全常用正则表达式大全(33081)
3. 基于Vue2.0+Vue-router构建一个简单的单页应用(23705)
4. JS获取当前时间戳的方法(23538)
5. jQuery中的text()、html()和val()以及innerText、innerHTML和value(23011)
评论排行榜
1. 2017我的个人总结：得与失(10)
2. React Native之APK文件签名及打包(6)
3. 基于Vue2.0+Vue-router构建一个简单的单页应用(4)
4. 使用IntelliJ IDEA和Maven构建Java web项目并打包部署(3)
5. 跨平台开发之阿里Weex框架环境搭建（一）(3)
推荐排行榜
1. 2017我的个人总结：得与失(6)
2. 史上最全常用正则表达式大全(4)
3. 百度地图实现鼠标绘制多边形并获取所有点坐标(3)
4. 一篇迟到的gulp文章，代码合并压缩，
