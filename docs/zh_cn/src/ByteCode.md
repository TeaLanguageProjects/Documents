# Tea语言虚拟机字节码

以下列出的是Tea语言虚拟机的字节码列表表格。

由于项目正在开发中，您现在看到的内容可能会在将来被修改。

在Tea语言中，字节码长度为2个字节（0x00 00 - 0xFF FF）。

| 二进制字节  | 助记符号  |  参数      | 描述   |
| :---------- | :----:     | :--------: | :----- |
| 0x00 | NOP | - | 不执行任何操作 |
| 0x01 | PUSH_NULL | - | 将NULL值Push到本地栈 |
| 0x02 | PUSH_FROM_BYTE_VAR | (Long)DataID | 将指定的byte类型变量Push到本地栈 |
| 0x03 | PUSH_FROM_SHORT_VAR | (Long)DataID | 将指定的short类型变量Push到本地栈 |
| 0x04 | PUSH_FROM_INT_VAR | (Long)DataID | 将指定的int类型变量Push到本地栈 |
| 0x05 | PUSH_FROM_LONG_VAR | (Long)DataID | 将指定的long类型变量Push到本地栈 |
| 0x06 | PUSH_FROM_FLOAT_VAR | (Long)DataID | 将指定的float类型变量Push到本地栈 |
| 0x07 | PUSH_FROM_DOUBLE_VAR | (Long)DataID | 将指定的double类型变量Push到本地栈 |
| 0x08 | PUSH_FROM_CHAR_VAR | (Long)DataID | 将指定的char类型变量Push到本地栈 |
| 0x09 | PUSH_FROM_BYTE_CONST | (Long)DataID | 将指定的byte类型本地常量Push到本地栈 |
| 0x0A | PUSH_FROM_SHORT_CONST | (Long)DataID | 将指定的short类型本地常量Push到本地栈 |
| 0x0B | PUSH_FROM_INT_CONST | (Long)DataID | 将指定的int类型本地常量Push到本地栈 |
| 0x0C | PUSH_FROM_LONG_CONST | (Long)DataID | 将指定的long类型本地常量Push到本地栈 |
| 0x0D | PUSH_FROM_FLOAT_CONST | (Long)DataID | 将指定的float类型本地常量Push到本地栈 |
| 0x0E | PUSH_FROM_DOUBLE_CONST | (Long)DataID | 将指定的double类型本地常量Push到本地栈 |
| 0x0F | PUSH_FROM_CHAR_CONST | (Long)DataID | 将指定的char类型本地常量Push到本地栈 |







