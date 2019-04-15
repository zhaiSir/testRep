
[地址：https://blog.csdn.net/sufu1065/article/details/88051083](https://blog.csdn.net/sufu1065/article/details/88051083 )

数据类型 　　大小             范围                                     默认值    
byte(字节) 　  8          -128  - 127                                 0   
shot(短整型) 　16       -32768 - 32768                                0    
int(整型) 　　 32     -2147483648-2147483648                          0    
float(浮点型)  32  -3.40292347E+38-3.40292347E+38                     0.0f   
double(双精度) 64 -1.79769313486231570E+308-1.79769313486231570E+308  0.0d   
char(字符型)   16      ‘ \u0000 - u\ffff ’                           ‘\u0000 ’   
boolean(布尔型) 1 true/false                                          false   

分类为：  
　　逻辑类 boolean   
　　文本类 char   
　　整数类 byte, short, int, long  
　　浮点类 double, float。  

##1. JRE和JDK的区别
>https://blog.csdn.net/shaochenshuo/article/details/78507132   
**JDK**：<font color=red>开发java程序用的开发包</font>,其中包括client和server端的，需要配置环境变量，
<font color=blue>Jdk包含**jre**</font>。    
**JRE**：<font color=red>java运行环境</font>，JRE里面只有client运行环境，安装过程中，会自动添加PATH，
<font color=red>Jre包含**jvm（虚拟机）**</font>,还有所有java类库的class文件，都在lib目录下打包成了jar。 

##2. == 和 equals 的区别是什么？
><font color="blue">== 的作用：</font>   
　　基本类型：比较的就是值是否相同   
　　引用类型：比较的就是地址值是否相同   
<font color="blue">equals 的作用:</font>    
　　比较的是两个字符串或对象的内容，属于内容比较。
 
<font color="red">总结：</font>
equals与==是等效的（Object类中的equals没什么区别），不同的原因就在于有些类（像String、Integer等类）对equals进行了重写。

****
补充几点：   
1、新建一个类，尤其是业务相关的对象类的时候，最好复写equals方法。   
2、复写equals方法时，同时记着要复写hashCode方法，谁能保证说这个对象一定不会出现在hashMap中呢？如果你用的是eclipse的自动代码生成，你会发现eclipse中复写equals和hashCode是在一起的。

引申出几个经常在面试中问到的问题：   
     1、两个对象，如果a.equals(b)==true，那么a和b是否相等？      
          相等，但地址不一定相等。   
     <font color="green">2、两个对象，如果hashcode一样，那么两个对象是否相等？   
          不一定相等，判断两个对象是否相等，需要判断equals是否为true。</font>       
 
 ```解答：   
如果我们对一个对象重写了euqals，意思是只要对象的成员变量值都相等那么euqals就等于true，
但不重写hashcode，那么我们再new一个新的对象，当原对象.equals（新对象）等于true时,
两者的hashcode却是不一样的，由此将产生了理解的不一致。```   