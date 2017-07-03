# w8scan 一款模仿bugscan的扫描器

## 前言
说是模仿bugscan,但是我并没有bugscan账号，我所做的是模仿他的通信原理。网页端返回一段代码，本地python环境执行上述代码即可扫描。
### 具体流程：
web端提供一个链接 -> 节点运行 ->在web端可进行在线扫描等的操作

### 本扫描器主要特点
- 就两点，使用简单，安装简单。

## 安装环境
小菜使用了很多大神的扫描器，但是安装太过于复杂，于是暗自下决心，自己写的一定要简单好用

- 只需要拥有一个php+mysql环境（本地外地均可）
- 安装网站：导入sql，ok，扫描器安装成功了。
- 使用：进入扫描器新增目标，按照提示执行python命令即可

### 备注说明1
因为之前用其他大牛开发的工具，有一大堆的依赖库。所以自己开发的东西尽量没有使用第三方库，所有功能都由python的内置库打造。（集成了 hackhttp等库，不用额外安装）

### 备注说明2
扫描器可为个人和安全团队作为内部扫描器使用。扫描器切勿用于非法用途！！

## 开发想法
1. 通过python的脚本执行特性，从网页上下载代码来执行，只需要在某个节点执行 python xxx 即可进行扫描  
2. 扫描规则通过web端进行配置，web指纹,exp等等可以web端上配置 
3. web端基于php+mysql 不需要很多要求，一个空间足矣

扫描器内置了bugscan的hackhttp模块

## 图片展示
首页
![1](https://user-images.githubusercontent.com/18695984/27781327-f4cfc320-5fff-11e7-81be-c5281c140551.jpg)

加入任务完成后 在本地执行命令即可
![4](https://user-images.githubusercontent.com/18695984/27781403-4bb7451e-6000-11e7-97a1-08698042f052.jpg)
![5](https://user-images.githubusercontent.com/18695984/27781404-4bba7a90-6000-11e7-8ce4-8a0464fc55e0.jpg)
任务管理可查看任务

会自动生成漏洞报告

## 插件管理和指纹管理的网页端没有写完
我觉得这个写在网页端不如直接上传到空间实在。