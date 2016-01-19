# Sky Walking
SkyWalking-Distributed Application Tracing System, 是一个对JAVA应用程序运行情况进行追踪、告警和分析的系统。
* 核心理论为[Google Dapper论文：Dapper, a Large-Scale Distributed Systems Tracing Infrastructure](http://research.google.com/pubs/pub36356.html),英语有困难的同学可参考[国内翻译](http://duanple.blog.163.com/blog/static/70971767201329113141336/)
* 本分析系统能通过不修改或少量修改代码的模式，对现有的JAVA应用或J2EE应用进行监控和数据收集，并针对应用进场进行准实时告警。此外提供大量的调用性能分析功能，解决目前的监控系统主要监控进程、端口而非应用实际性能的问题。

# 主要贡献者
* 吴晟 &nbsp;&nbsp;[亚信](http://www.asiainfo.com/) wusheng@asiainfo.com
* 张鑫 &nbsp;&nbsp;[亚信](http://www.asiainfo.com/) zhangxin10@asiainfo.com

# 整体架构图
![整体架构图](http://wu-sheng.github.io/sky-walking/sample-code/images/skywalkingClusterDeploy.jpeg)

# 追踪链路图
![追踪连路途](http://wu-sheng.github.io/sky-walking/sample-code/images/traceLogView.jpeg)

# Home Page
http://wu-sheng.github.io/sky-walking/

# API Guide
http://wu-sheng.github.io/sky-walking/sample-code/codeView.html

# Contact Us
Mail: wu.sheng@foxmail.com

# Quick Start
## 根据所需的监控点，引入maven依赖（暂不存在公网仓库，需要本地编译并发布）
```xml
<!-- Spring插件，监控所有Spring托管对象的调用-->
<dependency>
    <groupId>com.ai.cloud</groupId>
    <artifactId>skywalking-spring-plugin</artifactId>
    <version>1.0-SNAPSHOT</version>
</dependency>
<!-- dubbo插件，监控dubbo/dubbox调用 -->
<dependency>
    <groupId>com.ai.cloud</groupId>
    <artifactId>skywalking-dubbo-plugin</artifactId>
    <version>1.0-SNAPSHOT</version>
</dependency>
<!-- jdbc插件，监控所有的jdbc调用 -->
<dependency>
    <groupId>com.ai.cloud</groupId>
    <artifactId>skywalking-jdbc-plugin</artifactId>
    <version>1.0-SNAPSHOT</version>
</dependency>
<!-- httpClient插件，监控httpClient 4.2的调用 -->
<dependency>
    <groupId>com.ai.cloud</groupId>
    <artifactId>skywalking-httpClient-4.2.x-plugin</artifactId>
    <version>1.0-SNAPSHOT</version>
</dependency>
<!-- httpClient插件，监控httpClient 4.3的调用 -->
<dependency>
    <groupId>com.ai.cloud</groupId>
    <artifactId>skywalking-httpClient-4.3.x-plugin</artifactId>
    <version>1.0-SNAPSHOT</version>
</dependency>
```

## 根据所需插件配置应用程序
参考[用户指南](http://wu-sheng.github.io/sky-walking/sample-code/codeView.html)

## 下载授权文件
通过skywalking-webui工程下载授权文件

## 在运行时环境中设置环境变量
export SKYWALKING_RUN=true
