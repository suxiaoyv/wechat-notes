 学东西最好的方法就是每一步都有输出，下边是我总结的自己以前学习道路上的一些阶段，
 其中有自己以前没有想到的，走了弯路的，放出来，大家共勉。

-  准备工作
    - 翻墙：如果你学习android 起码要能够阅读开发者文档，清晰了解和随时查看api文档，那么你需要google，需要随时查看developer.android.com，具体如何翻，请问刘看山；
    - 开发必备：google github git developer.android
    - 环境搭建：上一步准备完成了，那么你可以到developer.android.com上下载Android SDK，以及开发者工具AndroidStudio，到http://www.oracle.com/technetwork/java/javase/downloads/index-jsp-138363.html#javasejdk下载JDK（额，SUN被ORACLE收购了众所周知），然后先安装JDK，貌似现在SDK在AndroidStudio中集成了，你可以免去下载SDK的麻烦，安装一个AndroidStudio就可以了。
    - HelloWorld：打开AndroidStudio，新建一个项目，AndroidStudio中会有很多模板，选一个简单的吧，恩，然后运行一下，这个就是你的HelloWorld程序。
    - 详细阅读代码、了解代码结构：好好看，看都是什么，google下代码结构等。
    - 输出： 能够清晰了解每一块代码的用途
- 配置文件：
    - setting.gradle build.gradle local.properties  编译配置文件要好好了解
    - AndroidManifest.xml permission相关的东西，application相关，activity 注册，事件相关的也要好好了解
    - 输出：能够清晰的了解每个配置文件的职能以及配置项。
- UI界面 View控件布局学习
    - 原生控件都要好好看一看，看看都是怎么布局的
    - 输出：达到 能自定义View 能快速对设计稿切分布局
- Control控制层学习
    - Activity：生命周期相关，Intent启动相关等
    - Service：生命周期
    - Broadcast Receiver
    - ContentProvider
    - 事件回调处理
    - 四大控件交互 Hanler 等
    - 输出：如何交互，了解各个生命周期，并每个写出N个实例
- 数据存储
    - SharePreference
    - File
    - SQLite
    - ContentProvide
    - 输出：了解各个如何存储，并每个写出N个实例
- 网络编程
    - HTTP网络访问相关知识 GET POST等
    - JSON XML 等数据传输格式如何解析
    - 输出：能够从开放API 如https://developer.github.com/v3/获取api 并解析
- 异常处理： CrashHandler DeviceInfo 等
- 输出：做一个小的程序，不需要界面华丽，能把自己学得知识都用上去就好。


     最后：
     你可能需要一个服务器，别担心，现在云服务那么发达，UCloud就不错(https://www.ucloud.cn/)，你可能要写服务器代码，nodejs可以很容易搭建一个服务器。
     附上自己最近开的一个公众号 yushaosxy
