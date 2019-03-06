地址：https://blog.csdn.net/sufu1065/article/details/88051083   

人见人爱

麻雀虽小，五脏俱全。

寥寥无几


Spring 框架 ---> 生态

Spring三阶段
  
配置阶段：主要是完成application.xml配置和Annotation配置。

初始化阶段：主要是加载并解析配置信息，然后，初始化IOC容器，完成容器的DI操作，已经完成HandlerMapping的初始化。

运行阶段：主要是完成Spring容器启动以后，完成用户请求的内部调度，并返回响应结果。

##1.JRE和JDK的区别
>https://blog.csdn.net/shaochenshuo/article/details/78507132   
**JDK**：<font color=red>开发java程序用的开发包</font>,其中包括client和server端的，需要配置环境变量，
<font color=blue>Jdk包含**jre**</font>。    
**JRE**：<font color=red>java运行环境</font>，JRE里面只有client运行环境，安装过程中，会自动添加PATH，
<font color=red>Jre包含**jvm（虚拟机）**</font>,还有所有java类库的class文件，都在lib目录下打包成了jar。 
