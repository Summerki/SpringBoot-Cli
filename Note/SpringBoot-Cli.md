---
typora-copy-images-to: images
---

[TOC]

[TOC]

> 自用SpringBoot脚手架，很简单的一个脚手架，自己开发时可以省去很多麻烦
>
> 就叫SpringBoot-Cli吧
>
> 本Note存储有关搭建SpringBoot-Cli时的笔记

## 1、SpringBoot版本

该`SpringBoot-Cli`基于SpringBoot`2.2.5`版本

需要更改SpringBoot版本请修改`pom.xml`，如下：

![1583152404455](images/1583152404455.png)

## 2、初始化工作

确定完版本之后，接下来是修改项目名，包名等初始化工作

在`pom.xml`里面修改`<groupId>`、`<artifactId>`、`<version>`、`<name>`以及`<description>`方法如下：

![1583152654961](images/1583152654961.png)

注，其中的`<name>`标签对应maven插件的名字，如下：

![1583152760941](images/1583152760941.png)

---

最后确认一下java的版本，`SpringBoot-Cli`使用`java 1.8`版本

![1583152935664](images/1583152935664.png)

## 3、修改模块名、基础包名和启动类名

![1583153183730](images/1583153183730.png)

将`SpringBoot-Cli`用IDEA打开后，会看到如上图所示根文件夹；其中`demo3`为模块名，`demo111`是其在电脑上文件夹的名称

右键`Refactor->Rename`可以更改模块名

---

在`SpringBoot-Cli`根包右键`Refactor->Rename`可以更改包名，记得选择如下所示选项，这样才能成功更改包名，不然只会更改文件夹的名称

![1583153508333](images/1583153508333.png)

---

同理，修改启动类的名称也是`Refactor->Rename`，记得选择下面三项：

![1583153673545](images/1583153673545.png)

## 4、resources文件夹

> 为了实现线上部署和开发时都可以有效的调试界面，我给出以下两种文件放置方式可供选择；分别是不使用模板引擎和使用模板引擎的文件放置配置方式

### 4.1、不使用模板引擎

在`pom.xml`里面去除`thymeleaf`依赖，我们使用SpringMVC来完成跳转的功能





