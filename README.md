# AUL
AUL(MyDUL)工具简介
从2005年开始，AUL (MyDUL)已经为全球不同国家及地区的众多客户恢复了数十TB计的Oracle数据，从损坏的Oracle 8, Oracle 8i, Oracle 9i, Oracle 10g, Oracle 11g及Oracle ASM上为客户快速恢复数据. AUL(MyDUL)可以脱离Oracle运行环境，直接从数据文件中读取记录，与官方工具Oracle DUL具有同等功效并且功能更加丰富。当你遇到下列极端情况，并且没有有效备份(客户有备份动作，备份不起作用的情况也遇到过)用来恢复数据时, AUL(MyDUL)是往往是你最后的机会. 一直坚持“拯救数据，帮助客户”的原则！在最新版本AUL 6中, 可以直接访问Oracle ASM来恢复数据，或从Oracle ASM中将数据文件拷贝出来。

1. 完全丢失系统表空间
2. 系统表空间有坏块
3. 表空间被删除，但数据文件还存在
4. 表被删除后，马上停止操作，空间未被重用
5. 表被清空(Truncate)后马上停止操作，空间未被重用
6. 一个表空间丢失了部份文件，或文件中有坏块，无法自我修复
7. Oracle ASM存贮损坏，或Oracle ASM磁盘损坏
8. 其他无法正常打开数据库或无法查询数据的情况
    AUL(MyDUL)并不提供免费服务，没有许可证的情况下最多允许同时打开10个数据文件，并且只能访问文件的前512MB内容，要支持更多的数据文件或更大的数据文件恢复，你必须获得许可证并在使用前进行注册。

    另外一个免费工具AUL for Oracle ASM (下载)可以将存放在Oracle ASM中的数据文件拷到文件系统， 在Oracle ASM损坏或磁盘不可用时，进行文件级的数据恢复，在AUL(MyDUL 6)中也集成了这个工具的所有功能，并且免费使用，最大支持2028块盘的Oracle ASM存贮。

AUL(MyDUL)功能列表
支持Oracle 8/8i/9i/10g/10g/11g等不同版本
直接访问Oracle ASM存贮，无需先将文件拷出来
从损坏的Oracle ASM中拷出数据文件到文件系统
支持普通表(Table)/聚族(Cluster)/索引组织表(IOT)
数据类型支持
NUMBER
DATE
CHAR
NCHAR
VARCHAR2
NVARCHAR2
RAW
LONG
LONG RAW
BINARY_FLOAT
BINARY_DOUBLE
TIMESTAMP
TIMESTAMP WITH TIME ZONE
可以将数据恢复成格式化文本文件，或者Oracle 8.1.7版本的DMP格式文件
在System表空间有效的情况下，可以自动生成SQL*Loader控制文件，方便数据装载
使用标准C语方编写，可以运行在Windows (VC6), Linux (gcc), Solaris (gcc)等不同平台上
支持跨平台交叉恢复，比如在Windows上也可以恢复AIX下的Oracle数据库
CLOB/BLOB支持
支持inline-lob, enable storage in row LOB和disable storage in row LOB.
支持不同CHUNK大小的CLOB/BLOB，同一个表不同的LOB CHUNK大小不支持.
CLOB/BLOB数据可以导出成独立的文件，或者DMP格式文件.
集成ICONV库，支持CLOB字符集转换.
无System表空间的CLOB/BLOB数据恢复.
从AUl 5版本开始支持压缩(Compress)表.
从AUl 5版本开始支持压缩(Compress)的索引组织表(IOT).
AUL(MyDUL)不支持的功能
Oracle 7版本
BFILE数据类型
Oracle对象数据类型(例如Spatial Data等)
    AUL(MyDUL)并不提供免费服务，没有许可证的情况下最多允许同时打开10个数据文件，并且只能访问文件的前512MB内容，要支持更多的数据文件或更大的数据文件恢复，你必须获得许可证并在使用前进行注册。
