---
title: 安装Java环境（JDK）
description: Download, install, and set up InfluxDB OSS.
menu: jdk_1_8
weight: 3

---

Java运行环境是每个java开发人员必须会的基础。

{{< tabs-wrapper >}}
{{% tabs %}}
[Linux](#)
[Windows](#)
[macOS](#)
[Docker](#)

{{% /tabs %}}

<!-------------------------------- BEGIN Linux -------------------------------->
{{% tab-content %}}

### 下载Linux的JDK

下载适用Linux的jdk安装文件，下载前需要先登录Oracle官网，如果没有账号需要注册一个账号。

<a class="btn download" href="https://download.oracle.com/otn/java/jdk/8u311-b11/4d5417147a92418ea8b615e228bb6935/jdk-8u311-linux-i586.tar.gz" download >Jdk1.8_311 (amd64)</a>

或者您可以在oracle官网[https://www.oracle.com/java/technologies/downloads/#java8](https://www.oracle.com/java/technologies/downloads/#java8)中下载适合的版本。

### 安装

1. 创建安装目录

   ```bash
   mkdir /usr/local/java/
   ```

2. 减压至安装目录

   ```bash
   tar -zxvf jdk-8u171-linux-x64.tar.gz -C /usr/local/java/
   ```

### 设置环境变量

1. 打开文件

   ```bash
   vim /etc/profile
   ```

2. 末尾添加环境变量

   ```bash
   export JAVA_HOME=/usr/local/java/jdk1.8.0_311
   export JRE_HOME=${JAVA_HOME}/jre
   export CLASSPATH=.:${JAVA_HOME}/lib:${JRE_HOME}/lib
   export PATH=${JAVA_HOME}/bin:$PATH
   ```

   _**注意:** jdk1.8.0_311要根据实际您下载的版本号进行调整。_

3. 使变量生效

   ```bash
   source /etc/profile
   ```

4. 验证是否安装成功

   ```bash
   java -version
   ```

{{% /tab-content %}}
<!--------------------------------- END Linux --------------------------------->

<!------------------------------- BEGIN Windows ------------------------------->
{{% tab-content %}}

### 下载JDK

下载适用Windows的jdk安装文件，下载前需要先登录Oracle官网，如果没有账号需要注册一个账号。

<a class="btn download" href="https://download.oracle.com/otn/java/jdk/8u311-b11/4d5417147a92418ea8b615e228bb6935/jdk-8u311-windows-i586.exe" download >Jdk1.8_311 (x86)</a>  <a class="btn download" href="https://download.oracle.com/otn/java/jdk/8u311-b11/4d5417147a92418ea8b615e228bb6935/jdk-8u311-windows-x64.exe" download >Jdk1.8_311 (x64)</a>

或者您可以在oracle官网[https://www.oracle.com/java/technologies/downloads/#java8-windows](https://www.oracle.com/java/technologies/downloads/#java8-windows)中下载适合的版本。

### 安装

只需要双击运行，一直点下一步就可以。

### 设置环境变量

1. 右键计算机（此电脑、我的电脑），点击属性，点击高级系统设置，在弹出的系统属性页面，在高级页签，点击下面的环境变量按钮，进行配置系统环境变量。
2. 配置JAVA_HOME。新建，变量名`JAVA_HOME`，变量值，jdk路径，我的路径是`C:\Program Files\Java\jdk1.8.0_121`，保存。
3. 配置CLASSPATH。新建，变量名`CLASSPATH`，变量值，`.;%JAVA_HOME%\lib;%JAVA_HOME%\lib\tools.jar`（第一个分号前前面有一个点）。
4. 配置Path。打开`Path`变量，在变量值最前加入`%JAVA_HOME%\bin;%JAVA_HOME%\jre\bin;`

### 验证

运行cmd，输入java -version，显示java版本则成功。



{{% /tab-content %}}
<!-------------------------------- END Windows -------------------------------->

<!-------------------------------- BEGIN macOS -------------------------------->
{{% tab-content %}}

{{% note %}}

#### 我没有Mac电脑。。。

这是个悲伤的故事。。。

{{% /note %}}

{{% /tab-content %}}
<!--------------------------------- END macOS --------------------------------->

<!-------------------------------- BEGIN Docker ------------------------------->
{{% tab-content %}}

### 下载并允许Jdk

使用`docker run` 下载并运行jdk的 Docker 镜像.

```bash
待完成
```

{{% /tab-content %}}
<!--------------------------------- END Docker -------------------------------->

{{< /tabs-wrapper >}}
