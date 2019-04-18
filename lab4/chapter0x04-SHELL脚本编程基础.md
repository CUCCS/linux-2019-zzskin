# 第四章：SHELL脚本编程基础

## 任务一：用bash编写一个图片批处理脚本，实现以下功能：
### 1. 支持命令行参数方式使用不同功能

![image](image/imagepre01.png)

### 2. 支持对指定目录下所有支持格式的图片文件进行批处理
- 见代码
### 3. 支持以下常见图片批处理功能的单独使用或组合使用
- 支持对jpeg格式图片进行图片质量压缩

![image](image/image-compress1.png)

- 支持对jpeg/png/svg格式图片在保持原始宽高比的前提下压缩分辨率

![image](image/image-compress2.png)

- 支持对图片批量添加自定义文本水印

添加前：

![image](image/source1.png)

添加后：

![image](image/watermark_1.png)

- 支持批量重命名（统一添加文件名前缀或后缀，不影响原始文件扩展名）

前缀：

![image](image/rename1.png)

后缀：

![image](image/rename2.png)

- 支持将png/svg图片统一转换为jpg格式图片

![image](image/alljpg.png)

## 任务二：用bash编写一个文本批处理脚本，对以下附件分别进行批量处理完成相应的数据统计任务：
- [2014世界杯运动员数据](http://sec.cuc.edu.cn/huangwei/course/LinuxSysAdmin/exp/chap0x04/worldcupplayerinfo.tsv)
    - 统计不同年龄区间范围（20岁以下、[20-30]、30岁以上）的球员数量、百分比
    - 统计不同场上位置的球员数量、百分比
    - 名字最长的球员是谁？名字最短的球员是谁？
    - 年龄最大的球员是谁？年龄最小的球员是谁？

![image](image/worldcup1.png)



## 任务三：用bash编写一个文本批处理脚本，对以下附件分别进行批量处理完成相应的数据统计任务
- Web服务器访问日志

![image](image/web_log1.png)

- 统计访问来源主机TOP 100和分别对应出现的总次数

![image](image/web_log2.png)

- 统计访问来源主机TOP 100 IP和分别对应出现的总次数

![image](image/web_log3.png)

- 统计最频繁被访问的URL TOP 100

![image](image/web_log4.png)

- 统计不同响应状态码的出现次数和对应百分比

![image](image/web_log5.png)

- 分别统计不同4XX状态码对应的TOP 10 URL和对应出现的总次数

![image](image/web_log6.png)

- 给定URL输出TOP 100访问来源主机

![image](image/web_log7.png)

## 注意事项：
1. awk -F 分隔符的选择
2. echo -e "\n\t" echo如何输出制表符和换行符
3. file命令判断文件真实格式
4. ImageMagic做图像处理
5. 正则表达式的使用（去空格、保留文件名等）
6. getopts的使用
7. awk语法