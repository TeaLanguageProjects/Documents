# Tea语言虚拟机字节码

以下列出的是Tea语言虚拟机的字节码列表表格。

由于项目正在开发中，您现在看到的内容可能会在将来被修改。

在Tea语言中，字节码长度为2个字节（0x0000 - 0xFFFF）。

同时需要注意的是，在这一版本的TeaVM虚拟机中，栈分为类本地栈和虚拟机主栈。

每个类都拥有独立的类本地栈，但虚拟机主栈是唯一的。

如果没有说明是本地栈还是虚拟机栈，则默认为本地栈。

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
| 0x1D      | PUSHVM_FROM_BYTE_CONST  | (Long)DataID   | 从本地常量推送byte常量到虚拟机栈        |
| 0x1E      | PUSHVM_FROM_SHORT_CONST | (Long)DataID   | 从本地常量推送short常量到虚拟机栈       |
| 0x1F      | PUSHVM_FROM_INT_CONST   | (Long)DataID   | 从本地常量推送int常量到虚拟机栈         |
| 0x20      | PUSHVM_FROM_LONG_CONST  | (Long)DataID   | 从本地常量推送long常量到虚拟机栈        |
| 0x21      | PUSHVM_FROM_FLOAT_CONST | (Long)DataID   | 从本地常量推送float常量到虚拟机栈       |
| 0x22      | PUSHVM_FROM_DOUBLE_CONST | (Long)DataID  | 从本地常量推送double常量到虚拟机栈      |
| 0x23      | PUSHVM_FROM_CHAR_CONST  | (Long)DataID   | 从本地常量推送char常量到虚拟机栈        |
| 0x24      | POPVM_TO_BYTE_VAR       | (Long)DataID   | 从虚拟机栈弹出byte值并存储到变量中      |
| 0x25      | POPVM_TO_SHORT_VAR      | (Long)DataID   | 从虚拟机栈弹出short值并存储到变量中     |
| 0x26      | POPVM_TO_INT_VAR        | (Long)DataID   | 从虚拟机栈弹出int值并存储到变量中       |
| 0x27      | POPVM_TO_LONG_VAR       | (Long)DataID   | 从虚拟机栈弹出long值并存储到变量中      |
| 0x28      | POPVM_TO_FLOAT_VAR      | (Long)DataID   | 从虚拟机栈弹出float值并存储到变量中     |
| 0x29      | POPVM_TO_DOUBLE_VAR     | (Long)DataID   | 从虚拟机栈弹出double值并存储到变量中    |
| 0x2A      | POPVM_TO_CHAR_VAR       | (Long)DataID   | 从虚拟机栈弹出char值并存储到变量中      |
| 0x2B      | PUSHVM_FROM_BYTE_VAR      | (Long)DataID    | 将byte变量推送到虚拟机栈                    |
| 0x2C      | PUSHVM_FROM_SHORT_VAR     | (Long)DataID    | 将short变量推送到虚拟机栈                   |
| 0x2D      | PUSHVM_FROM_INT_VAR       | (Long)DataID    | 将int变量推送到虚拟机栈                     |
| 0x2E      | PUSHVM_FROM_LONG_VAR      | (Long)DataID    | 将long变量推送到虚拟机栈                    |
| 0x2F      | PUSHVM_FROM_FLOAT_VAR     | (Long)DataID    | 将float变量推送到虚拟机栈                   |
| 0x30      | PUSHVM_FROM_DOUBLE_VAR    | (Long)DataID    | 将double变量推送到虚拟机栈                  |
| 0x31      | PUSHVM_FROM_CHAR_VAR      | (Long)DataID    | 将char变量推送到虚拟机栈                    |
| 0x32      | PUSHVM_FROM_BYTE_VMCONST  | (Long)DataID    | 从虚拟机常量推送byte常量到虚拟机栈           |
| 0x33      | PUSHVM_FROM_SHORT_VMCONST | (Long)DataID    | 从虚拟机常量推送short常量到虚拟机栈          |
| 0x34      | PUSHVM_FROM_INT_VMCONST   | (Long)DataID    | 从虚拟机常量推送int常量到虚拟机栈            |
| 0x35      | PUSHVM_FROM_LONG_VMCONST  | (Long)DataID    | 从虚拟机常量推送long常量到虚拟机栈           |
| 0x36      | PUSHVM_FROM_FLOAT_VMCONST | (Long)DataID    | 从虚拟机常量推送float常量到虚拟机栈          |
| 0x37      | PUSHVM_FROM_DOUBLE_VMCONST| (Long)DataID    | 从虚拟机常量推送double常量到虚拟机栈         |
| 0x38      | PUSHVM_FROM_CHAR_VMCONST  | (Long)DataID    | 从虚拟机常量推送char常量到虚拟机栈           |
| 0x39      | PUSH_FROM_LINK_VAR        | (Long)DataID    | 从LINK变量推送值到本地栈                     |
| 0x3A      | PUSH_FROM_LINK_CONST      | (Long)DataID    | 从LINK常量推送值到本地栈                     |
| 0x3B      | PUSH_FROM_LINK_VMCONST    | (Long)DataID    | 从虚拟机常量推送link常量到本地栈             |
| 0x3C      | POP_TO_LINK_VAR           | (Long)DataID    | 从本地栈弹出link值并存储到变量中              |
| 0x3D      | PUSHVM_FROM_LINK_VAR      | (Long)DataID    | 从link变量推送值到虚拟机栈                   |
| 0x3E      | PUSHVM_FROM_LINK_CONST    | (Long)DataID    | 从link常量推送值到虚拟机栈                   |
| 0x3F      | PUSHVM_FROM_LINK_VMCONST  | (Long)DataID    | 从虚拟机常量推送link常量到虚拟机栈           |
| 0x40      | POP_NULL                  | -               | 从本地栈弹出一个值，但不执行任何操作                   |
| 0x41      | INT_TO_FLOAT         | -            | 将本地栈顶的int类型值转换为float类型值                |
| 0x42      | INT_TO_LONG          | -            | 将本地栈顶的int类型值转换为long类型值                 |
| 0x43      | INT_TO_DOUBLE        | -            | 将本地栈顶的int类型值转换为double类型值               |
| 0x44      | FLOAT_TO_INT         | -            | 将本地栈顶的float类型值转换为int类型值                |
| 0x45      | FLOAT_TO_LONG        | -            | 将本地栈顶的float类型值转换为long类型值               |
| 0x46      | FLOAT_TO_DOUBLE      | -            | 将本地栈顶的float类型值转换为double类型值             |
| 0x47      | LONG_TO_INT          | -            | 将本地栈顶的long类型值转换为int类型值                 |
| 0x48      | LONG_TO_FLOAT        | -            | 将本地栈顶的long类型值转换为float类型值                |
| 0x49      | LONG_TO_DOUBLE       | -            | 将本地栈顶的long类型值转换为double类型值               |
| 0x4A      | DOUBLE_TO_INT        | -            | 将本地栈顶的double类型值转换为int类型值                |
| 0x4B      | DOUBLE_TO_FLOAT      | -            | 将本地栈顶的double类型值转换为float类型值              |
| 0x4C      | DOUBLE_TO_LONG       | -            | 将本地栈顶的double类型值转换为long类型值               |
| 0x4D      | INT_TO_BYTE          | -            | 将本地栈顶的int类型值截断为byte类型，然后通过符号扩展为int类型值并将其推送到本地栈上 |
| 0x4E      | INT_TO_SHORT         | -            | 将本地栈顶的int类型值截断为short类型，然后通过符号扩展为int类型值并将其推送到本地栈上 |
| 0x4F      | INT_TO_CHAR          | -            | 将本地栈顶的int类型值截断为char类型，然后通过符号扩展为int类型值并将其推送到本地栈上 |
| 0x50      | CHAR_TO_INT          | -            | 将本地栈顶的char类型值转换为int类型值                |
| 0x51      | SHORT_TO_INT         | -            | 将本地栈顶的short类型值转换为int类型值               |
| 0x52      | BYTE_TO_INT          | -            | 将本地栈顶的byte类型值转换为int类型值                |
| 0x53      | IADD               | -          | 将本地栈顶的两个int相加，并将结果推送到本地栈上                 |
| 0x54      | ISUB               | -          | 将本地栈顶的两个int相减，并将结果推送到本地栈上                 |
| 0x55      | IMUL               | -          | 将本地栈顶的两个int相乘，并将结果推送到本地栈上                 |
| 0x56      | IDIV               | -          | 将本地栈顶的两个int相除，并将结果推送到本地栈上                 |
| 0x57      | IREM               | -          | 将本地栈顶的两个int取余，并将结果推送到本地栈上                 |
| 0x58      | INEG               | -          | 将本地栈顶的int取负，并将结果推送到本地栈上                   |
| 0x59      | LADD               | -          | 将本地栈顶的两个long相加，并将结果推送到本地栈上                |
| 0x5A      | LSUB               | -          | 将本地栈顶的两个long相减，并将结果推送到本地栈上                |
| 0x5B      | LMUL               | -          | 将本地栈顶的两个long相乘，并将结果推送到本地栈上                |
| 0x5C      | LDIV               | -          | 将本地栈顶的两个long相除，并将结果推送到本地栈上                |
| 0x5D      | LREM               | -          | 将本地栈顶的两个long取余，并将结果推送到本地栈上                |
| 0x5E      | LNEG               | -          | 将本地栈顶的long取负，并将结果推送到本地栈上                  |
| 0x5F      | FADD               | -          | 将本地栈顶的两个float相加，并将结果推送到本地栈上               |
| 0x60      | FSUB               | -          | 将本地栈顶的两个float相减，并将结果推送到本地栈上               |
| 0x61      | FMUL               | -          | 将本地栈顶的两个float相乘，并将结果推送到本地栈上               |
| 0x62      | FDIV               | -          | 将本地栈顶的两个float相除，并将结果推送到本地栈上               |
| 0x63      | FREM               | -          | 将本地栈顶的两个float取余，并将结果推送到本地栈上               |
| 0x64      | FNEG               | -          | 将本地栈顶的float取负，并将结果推送到本地栈上                 |
| 0x65      | DADD               | -          | 将本地栈顶的两个double相加，并将结果推送到本地栈上              |
| 0x66      | DSUB               | -          | 将本地栈顶的两个double相减，并将结果推送到本地栈上              |
| 0x67      | DMUL               | -          | 将本地栈顶的两个double相乘，并将结果推送到本地栈上              |
| 0x68      | DDIV               | -          | 将本地栈顶的两个double相除，并将结果推送到本地栈上              |
| 0x69      | DREM               | -          | 将本地栈顶的两个double取余，并将结果推送到本地栈上              |
| 0x6A      | DNEG               | -          | 将本地栈顶的double取负，并将结果推送到本地栈上                |
| 0x6B      | ISHL               | -          | 将本地栈顶的int按指定位数左移，并将结果推送到本地栈上          |
| 0x6C      | ISHR               | -          | 将本地栈顶的int按指定位数右移，并将结果推送到本地栈上          |
| 0x6D      | IUSHR              | -          | 将本地栈顶的int按指定位数无符号右移，并将结果推送到本地栈上    |
| 0x6E      | LSHL               | -          | 将本地栈顶的long按指定位数左移，并将结果推送到本地栈上         |
| 0x6F      | LSHR               | -          | 将本地栈顶的long按指定位数右移，并将结果推送到本地栈上         |
| 0x70      | LUSHR              | -          | 将本地栈顶的long按指定位数无符号右移，并将结果推送到本地栈上   |
| 0x71      | IAND               | -          | 对本地栈顶的两个int执行按位与操作，并将结果推送到本地栈上        |
| 0x72      | IOR                | -          | 对本地栈顶的两个int执行按位或操作，并将结果推送到本地栈上        |
| 0x73      | IXOR               | -          | 对本地栈顶的两个int执行按位异或操作，并将结果推送到本地栈上      |
| 0x74      | LAND               | -          | 对本地栈顶的两个long执行按位与操作，并将结果推送到本地栈上       |
| 0x75      | LOR                | -          | 对本地栈顶的两个long执行按位或操作，并将结果推送到本地栈上       |
| 0x76      | LXOR               | -          | 对本地栈顶的两个long执行按位异或操作，并将结果推送到本地栈上     |
| 0x77      | IFEQ          | (Short)Offset | 如果本地栈顶的int值等于0，则跳转                  |
| 0x78      | IFNE          | (Short)Offset | 如果本地栈顶的int值不等于0，则跳转                |
| 0x79      | IFLT          | (Short)Offset | 如果本地栈顶的int值小于0，则跳转                  |
| 0x7A      | IFGE          | (Short)Offset | 如果本地栈顶的int值大于等于0，则跳转              |
| 0x7B      | IFGT          | (Short)Offset | 如果本地栈顶的int值大于0，则跳转                |
| 0x7C      | IFLE          | (Short)Offset | 如果本地栈顶的int值小于等于0，则跳转              |
| 0x7D      | IFNULL        | (Short)Offset | 如果本地栈顶的引用类型值为null，则跳转             |
| 0x7E      | IFNOTNULL     | (Short)Offset | 如果本地栈顶的引用类型值不为null，则跳转           |
| 0x7F      | GOTO          | (Short)Offset | 跳转到指定标签                              |
| 0x80      | IF_ICMPEQ     | (Short)Offset | 如果本地栈顶的两个int值相等，则跳转               |
| 0x81      | IF_ICMPNE     | (Short)Offset | 如果本地栈顶的两个int值不相等，则跳转             |
| 0x82      | IF_ICMPLT     | (Short)Offset | 如果本地栈顶的两个int值小于，则跳转               |
| 0x83      | IF_ICMPGE     | (Short)Offset | 如果本地栈顶的两个int值大于等于，则跳转           |
| 0x84      | IF_ICMPGT     | (Short)Offset | 如果本地栈顶的两个int值大于，则跳转             |
| 0x85      | IF_ICMPLE     | (Short)Offset | 如果本地栈顶的两个int值小于等于，则跳转           |
| 0x86      | IF_ACMPEQ     | (Short)Offset | 如果本地栈顶的两个引用类型值相等，则跳转          |
| 0x87      | IF_ACMPNE     | (Short)Offset | 如果本地栈顶的两个引用类型值不相等，则跳转        |
| 0x88      | ICMP          | -             | 比较本地栈顶的两个long值，前者较大则推送1；相等则推送0；后者较大则推送-1  |
| 0x89      | FCMP          | -             | 比较本地栈顶的两个float值，前者较大则推送1；相等则推送0；后者较大则推送-1 |
| 0x8A      | DCMP          | -             | 比较本地栈顶的两个double值，前者较大则推送1；相等则推送0；后者较大则推送-1 |
| 0x8B        | VM_INT_TO_FLOAT  | -               | 将虚拟机栈顶的int类型值转换为float类型值  |
| 0x8C        | VM_INT_TO_LONG   | -               | 将虚拟机栈顶的int类型值转换为long类型值   |
| 0x8D        | VM_INT_TO_DOUBLE | -               | 将虚拟机栈顶的int类型值转换为double类型值 |
| 0x8E        | VM_FLOAT_TO_INT  | -               | 将虚拟机栈顶的float类型值转换为int类型值  |
| 0x8F        | VM_FLOAT_TO_LONG | -               | 将虚拟机栈顶的float类型值转换为long类型值 |
| 0x90        | VM_FLOAT_TO_DOUBLE| -               | 将虚拟机栈顶的float类型值转换为double类型值|
| 0x91        | VM_LONG_TO_INT   | -               | 将虚拟机栈顶的long类型值转换为int类型值   |
| 0x92        | VM_LONG_TO_FLOAT | -               | 将虚拟机栈顶的long类型值转换为float类型值 |
| 0x93        | VM_LONG_TO_DOUBLE| -               | 将虚拟机栈顶的long类型值转换为double类型值|
| 0x94        | VM_DOUBLE_TO_INT | -               | 将虚拟机栈顶的double类型值转换为int类型值 |
| 0x95        | VM_DOUBLE_TO_FLOAT| -              | 将虚拟机栈顶的double类型值转换为float类型值|
| 0x96        | VM_DOUBLE_TO_LONG| -               | 将虚拟机栈顶的double类型值转换为long类型值 |
| 0x97        | VM_INT_TO_BYTE   | -               | 将虚拟机栈顶的int类型值转换为byte类型值  |
| 0x98        | VM_INT_TO_SHORT  | -               | 将虚拟机栈顶的int类型值转换为short类型值 |
| 0x99        | VM_INT_TO_CHAR   | -               | 将虚拟机栈顶的int类型值转换为char类型值  |
| 0x9A        | VM_CHAR_TO_INT   | -               | 将虚拟机栈顶的char类型值转换为int类型值  |
| 0x9B        | VM_SHORT_TO_INT  | -               | 将虚拟机栈顶的short类型值转换为int类型值 |
| 0x9C        | VM_BYTE_TO_INT   | -               | 将虚拟机栈顶的byte类型值转换为int类型值  |
| 0x9D        | VM_IADD          | -               | 将虚拟机栈顶的两个int值相加，并将结果压入虚拟机栈 |
| 0x9E        | VM_ISUB          | -               | 将虚拟机栈顶的两个int值相减，并将结果压入虚拟机栈 |
| 0x9F        | VM_IMUL          | -               | 将虚拟机栈顶的两个int值相乘，并将结果压入虚拟机栈 |
| 0xA0        | VM_IDIV          | -               | 将虚拟机栈顶的两个int值相除，并将结果压入虚拟机栈 |
| 0xA1        | VM_IREM          | -               | 将虚拟机栈顶的两个int值取余，并将结果压入虚拟机栈 |
| 0xA2        | VM_INEG          | -               | 将虚拟机栈顶的int值取负，并将结果压入虚拟机栈 |
| 0xA3        | VM_LADD          | -               | 将虚拟机栈顶的两个long值相加，并将结果压入虚拟机栈 |
| 0xA4        | VM_LSUB          | -               | 将虚拟机栈顶的两个long值相减，并将结果压入虚拟机栈 |
| 0xA5        | VM_LMUL          | -               | 将虚拟机栈顶的两个long值相乘，并将结果压入虚拟机栈 |
| 0xA6        | VM_LDIV          | -               | 将虚拟机栈顶的两个long值相除，并将结果压入虚拟机栈 |
| 0xA7        | VM_LREM          | -               | 将虚拟机栈顶的两个long值取余，并将结果压入虚拟机栈 |
| 0xA8        | VM_LNEG          | -               | 将虚拟机栈顶的long值取负，并将结果压入虚拟机栈 |
















