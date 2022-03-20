# Preparation

[TOC]

## 官网链接

1. 课程官方网站：[https://introcs.cs.princeton.edu/java/home/](https://introcs.cs.princeton.edu/java/home/)

2. 课程教材电子版链接：[**Computer Science An Interdisciplinary Approach**](https://github.com/TOMYUE/CS_self-learning/blob/main/Foundation/Java/CS61B/Book%20%26%20other%20material/Computer%20Science%20An%20Interdisciplinary%20Approach%20by%20Robert%20Sedgewick%2C%20Kevin%20Wayne.pdf)

3. 课程开发环境安装链接： [ [Mac OS X](https://introcs.cs.princeton.edu/java/mac) · [Windows](https://introcs.cs.princeton.edu/java/windows) · [Linux](https://introcs.cs.princeton.edu/java/11hello/linux.html) ]

4. 课程配备的Java标准库`Stdlib.jar`：https://introcs.cs.princeton.edu/java/stdlib/

5. 环境安装解决方案链接：

   1. Stack_Overflow:[Adding jar library to project Intellij IDEA](https://stackoverflow.com/questions/28270148/adding-jar-library-to-project-intellij-idea)

   2. Stack_Overflow:[How can I get stdlib.jar working in Intellij?](https://stackoverflow.com/questions/59111159/how-can-i-get-stdlib-jar-working-in-intellij)

   3. IDEAsupporter:[How to use stdlib.jar in Intellij Idea?](https://intellij-support.jetbrains.com/hc/en-us/community/posts/207703065-How-to-use-stdlib-jar-in-Intellij-Idea-)

   4. Youtube:[导入并使用Stdlib.jar的最佳解决方案](https://www.youtube.com/watch?v=M_QFaBwSaCw)

      > 上述方案中，==第4个==应该是最没有问题的方法。如果上述方法都不行，希望您也能在issue里告诉我，同时把您最后的解决方案如果能pull request的话感激不尽。

## 环境配置 

- 如果以前没有下载过Intellj IDEA，则按照官网教程完全没有问题，下载过的话，根据官网的FAQ来进行解决应该都没有大问题。

## 环境安装的困难点

==**解决Stdlib.jar难以使用的问题：**==

主机操作系统：Mac M1 （此方法应该在Windows中同样适用）

 Intellj IDEA：2021.3.3

 Java: openjdk-17



- 第一步：下载完成`Stdlib.jar`后，按照下图所示，鼠标右键（Mac为双指点按）点击您新建的项目文件，出现如下的界面，为了使其成为我们的内部库而不是外部库，我们新建一个Directory，并命名为lib

![image-20220320132757028](../../../../../../Library/Application%20Support/typora-user-images/image-20220320132757028.png)

- 第二步：将你下载的`Stdlib.jar`复制到lib这个文件夹下，然后点击File->Project Structure->Module如下图所示

![image-20220320132909833](../../../../../../Library/Application%20Support/typora-user-images/image-20220320132909833.png)

- 第三部，注意图片左侧的信息，点击Structure里的左侧Module，然后在如下的页面中选中Library->Java，然后系统会让您选择您要加载进入的`.jar`文件，默认出现的就像第四步中的图一样，是您当前的项目目录。

![image-20220320133026323](../../../../../../Library/Application%20Support/typora-user-images/image-20220320133026323.png)

- 第四步： 选中之前新建的lib文件夹（目录）中的`stdlib-package.jar`（此文件和`stdlib.jar`相同，发行时间不一样），然后点击右下角的`open`

![image-20220320133059694](../../../../../../Library/Application%20Support/typora-user-images/image-20220320133059694.png)

- 第五步：之后您就会回到下面这个页面，然后直接点击这个页面右下角的Apply在点击Ok就好了

![截屏2022-03-20 13.31.26](../../../../../../Desktop/%E6%88%AA%E5%B1%8F2022-03-20%2013.31.26.png)

- 第六步：您再次输入`Std`开头的命令，就会出现如下的提示符，这个时候就说明，您的安装就成功啦！

![image-20220320133225083](../../../../../../Library/Application%20Support/typora-user-images/image-20220320133225083.png)



![image-20220320133254734](../../../../../../Library/Application%20Support/typora-user-images/image-20220320133254734.png)

- 第七步：到此为止，所有Princeton提供的包都安装完成了，然后就开始开心的学习和编码了，Princeton所提供的Notes和Code Example质量都非常高，希望我们都能爱在其中！



## 其他

此配置环境过程的教程或解答在网络上不多，通过external的方式导入，因为本人水平问题始终没有成功，如上是权宜之计，如果您有更好的教程或解法望您能不吝赐教🤝！