# 类结构

以下列出的是在TeaVM虚拟机（HotTea）中每个类对象拥有的数据。

| 字段名称 | 中文名称 | 描述 | 
| :--- | :----: | :--- |
| LocalVariables | 本地变量表 | 存储类本地的变量数据 |
| LocalConstants | 本地常量表 | 存储类本地的常量数据 |
| ClassMetaData  | 类元数据   | 存储该类的附加信息（如编译时间，作者等） |
| LocalStack     | 本地栈     | 类本地栈，区分于虚拟机主栈（VMStack）和线程栈（ThreadStack） |
| LocalLinks     | 本地链接表 | 存储类本地的链接信息 |
| LocalImports   | 本地导入表 | 存储类引入外部包的类的链接（指针） |
| LocalFunctions | 本地函数表 | 存储类本地的函数（方法）的链接（指针） |
| LocalClasses   | 本地类表   | 存储类本地的内部类的链接（指针） |
| LocalIndex     | 本地类索引 | 存储类中字符串符号（如各种以字符串命名的变量）到类内部的ID的索引信息 |
| Type           | 类型       | 存储类的类型（普通类，函数或者接口等） |
| AccessModifier | 访问修饰符 | 存储类的访问修饰符 |
| NonAccessModifiers | 非访问修饰符 | 存储类的非访问修饰符 |
| Interfaces     | 接口 | 存储了类实现的接口的信息 |
| SuperClasses   | 父类 | 存储了类的父类 |
| Annotations    | 注解 | 存储了类的所有注解 |
| ClassName      | 类名       | - |
| PackageName    | 包名       | - |
| LocalData      | 本地数据   | 存储类的本地数据（如类的类型为函数，则存储程序代码） |

### 详细释义

1. **LocalVariables:**
   存储了该类所有的变量数据
2. **LocalConstants:**
   存储了该类所有的常量数据
3. **ClassMetaData:**
   存储了类编译时产生的元数据，包括但不限于：类的作者，类的编译时间，类使用的编译器版本，类的许可证等
4. **LocalStack:**
   类独立于虚拟机栈/线程栈的栈，在虚拟机运行时产生，用于存储类自身的栈数据。每个类都有独立于虚拟机的栈
5. **LocalLinks:**
   存储类的链接数据，如将外部类中的对象链接到本地类中，则在此表中添加数据
6. **LocalImports:**
   存储类引用的外部类的指针对象
7. **LocalFunctions:**
   存储类中包含的函数类的指针对象。调用函数时执行对应的函数类的本地数据中存储的程序代码
8. **LocalClasses:**
   存储类中包含的内部类的指针对象
9. **LocalIndex:**
    存储字符串和类中数据ID转换的索引数据，如一个字符串变量名为str1，在类中分配得到的数据ID为1001，则在该表中留下相应信息以便查询
10. **Type:**
    表明该类的类型，如普通类，接口，枚举，注解，函数等
11. **AccessModifier:**
    存储类的访问修饰符，如Public，Private等
12. **NonAccessModifiers:**
    存储类的非访问修饰符，如Static等
13. **Interfaces:**
    存储了类实现的接口的列表
14. **SuperClasses:**
    存储了类继承的父类的数据，在Tea语言中每个类只能继承一个类
15. **Annotations:**
    存储了类上的所有注解的信息
16. **ClassName:**
    此类的类名，用于区分相同软件包的不同类
17. **PackageName:**
    此类的包名，用于区分不同软件包的程序
18. **LocalData:**
    存储此类的数据，例如，如果类的类型是函数则存储程序代码
   
