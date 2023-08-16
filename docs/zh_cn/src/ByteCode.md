# Tea语言虚拟机字节码

以下列出的是Tea语言虚拟机的字节码列表表格。

由于项目正在开发中，您现在看到的内容可能会在将来被修改。

在Tea语言中，字节码长度为2个字节（0x0000 - 0xFFFF）。

同时需要注意的是，在这一版本的TeaVM虚拟机中，栈分为类本地栈和虚拟机主栈。

每个类都拥有独立的类本地栈，但虚拟机主栈是唯一的。

| 二进制字节  | 助记符号  |  参数      | 描述   |
| :---------- | :----:     | :--------: | :----- |
| 0x00 | NOP | - | 不执行任何操作 |
| 0x01 | PUSH_NULL | - | 将NULL值Push到本地栈 |
| 0x02 | PUSH_FROM_BYTE_VAR | (Long)DataID | 将指定的byte类型变量压入到本地栈 |
| 0x03 | PUSH_FROM_SHORT_VAR | (Long)DataID | 将指定的short类型变量压入到本地栈 |
| 0x04 | PUSH_FROM_INT_VAR | (Long)DataID | 将指定的int类型变量压入到本地栈 |
| 0x05 | PUSH_FROM_LONG_VAR | (Long)DataID | 将指定的long类型变量压入到本地栈 |
| 0x06 | PUSH_FROM_FLOAT_VAR | (Long)DataID | 将指定的float类型变量压入到本地栈 |
| 0x07 | PUSH_FROM_DOUBLE_VAR | (Long)DataID | 将指定的double类型变量压入到本地栈 |
| 0x08 | PUSH_FROM_CHAR_VAR | (Long)DataID | 将指定的char类型变量压入到本地栈 |
| 0x09 | PUSH_FROM_BYTE_CONST | (Long)DataID | 将指定的byte类型本地常量压入到本地栈 |
| 0x0A | PUSH_FROM_SHORT_CONST | (Long)DataID | 将指定的short类型本地常量压入到本地栈 |
| 0x0B | PUSH_FROM_INT_CONST | (Long)DataID | 将指定的int类型本地常量压入到本地栈 |
| 0x0C | PUSH_FROM_LONG_CONST | (Long)DataID | 将指定的long类型本地常量压入到本地栈 |
| 0x0D | PUSH_FROM_FLOAT_CONST | (Long)DataID | 将指定的float类型本地常量压入到本地栈 |
| 0x0E | PUSH_FROM_DOUBLE_CONST | (Long)DataID | 将指定的double类型本地常量压入到本地栈 |
| 0x0F | PUSH_FROM_CHAR_CONST | (Long)DataID | 将指定的char类型本地常量压入到本地栈 |
| 0x10      | POP_TO_BYTE_VAR      | (Long)DataID   | 从本地栈弹出byte值并存储到变量中         |
| 0x11      | POP_TO_SHORT_VAR     | (Long)DataID   | 从本地栈弹出short值并存储到变量中        |
| 0x12      | POP_TO_INT_VAR       | (Long)DataID   | 从本地栈弹出int值并存储到变量中          |
| 0x13      | POP_TO_LONG_VAR      | (Long)DataID   | 从本地栈弹出long值并存储到变量中         |
| 0x14      | POP_TO_FLOAT_VAR     | (Long)DataID   | 从本地栈弹出float值并存储到变量中        |
| 0x15      | POP_TO_DOUBLE_VAR    | (Long)DataID   | 从本地栈弹出double值并存储到变量中       |
| 0x16      | POP_TO_CHAR_VAR      | (Long)DataID   | 从本地栈弹出char值并存储到变量中         |
| 0x17      | PUSH_FROM_BYTE_VMCONST | (Long)DataID | 将指定的byte类型虚拟机常量压入到本地栈        |
| 0x18      | PUSH_FROM_SHORT_VMCONST | (Long)DataID | 将指定的short类型虚拟机常量压入到本地栈        |
| 0x19      | PUSH_FROM_INT_VMCONST | (Long)DataID   | 将指定的int类型虚拟机常量压入到本地栈        |
| 0x1A      | PUSH_FROM_LONG_VMCONST | (Long)DataID  | 将指定的long类型虚拟机常量压入到本地栈        |
| 0x1B      | PUSH_FROM_FLOAT_VMCONST | (Long)DataID | 将指定的float类型虚拟机常量压入到本地栈        |
| 0x1C      | PUSH_FROM_DOUBLE_VMCONST | (Long)DataID | 将指定的double类型虚拟机常量压入到本地栈        |
| 0x1D      | PUSHVM_FROM_BYTE_CONST  | (long)DataID   | 从本地常量推送byte常量到虚拟机栈        |
| 0x1E      | PUSHVM_FROM_SHORT_CONST | (long)DataID   | 从本地常量推送short常量到虚拟机栈       |
| 0x1F      | PUSHVM_FROM_INT_CONST   | (long)DataID   | 从本地常量推送int常量到虚拟机栈         |
| 0x20      | PUSHVM_FROM_LONG_CONST  | (long)DataID   | 从本地常量推送long常量到虚拟机栈        |
| 0x21      | PUSHVM_FROM_FLOAT_CONST | (long)DataID   | 从本地常量推送float常量到虚拟机栈       |
| 0x22      | PUSHVM_FROM_DOUBLE_CONST | (long)DataID  | 从本地常量推送double常量到虚拟机栈      |
| 0x23      | PUSHVM_FROM_CHAR_CONST  | (long)DataID   | 从本地常量推送char常量到虚拟机栈        |
| 0x24      | POPVM_TO_BYTE_VAR       | (long)DataID   | 从虚拟机栈弹出byte值并存储到变量中      |
| 0x25      | POPVM_TO_SHORT_VAR      | (long)DataID   | 从虚拟机栈弹出short值并存储到变量中     |
| 0x26      | POPVM_TO_INT_VAR        | (long)DataID   | 从虚拟机栈弹出int值并存储到变量中       |
| 0x27      | POPVM_TO_LONG_VAR       | (long)DataID   | 从虚拟机栈弹出long值并存储到变量中      |
| 0x28      | POPVM_TO_FLOAT_VAR      | (long)DataID   | 从虚拟机栈弹出float值并存储到变量中     |
| 0x29      | POPVM_TO_DOUBLE_VAR     | (long)DataID   | 从虚拟机栈弹出double值并存储到变量中    |
| 0x2A      | POPVM_TO_CHAR_VAR       | (long)DataID   | 从虚拟机栈弹出char值并存储到变量中      |

















