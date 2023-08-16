# 类架构

以下列出的是在TeaVM虚拟机中每个类对象拥有的数据。

| 字段名称 | 中文名称 | 描述 | 
| :--- | :----: | :--- |
| LocalVariables | 本地变量表 | 存储类本地的变量数据 |
| LocalConstants | 本地常量表 | 存储类本地的常量数据 |
| ClassMetaData  | 类元数据   | 存储该类的附加信息（如编译时间，作者等） |
| LocalStack     | 本地栈     | 类本地栈，区分于虚拟机主栈（VMStack） |
| LocalLinks     | 本地链接表 | 存储类本地的链接信息 |
| LocalImports   | 本地导入表 | 存储类引入外部包的类的链接（指针） |
| LocalFunctions | 本地函数表 | 存储类本地的函数（方法）的链接（指针） |
| LocalClasses   | 本地类表   | 存储类本地的内部类的链接（指针） |
| LocalIndex     | 本地类索引 | 存储类中字符串符号（如各种以字符串命名的变量）到类内部的ID的索引信息 |
| Type           | 类型       | 存储类的类型（普通类，函数或者接口等） |
| ClassName      | 类名       | - |
| PackageName    | 包名       | - |
| LocalData      | 本地数据   | 存储类的本地数据（如类的类型为函数，则存储程序代码） |