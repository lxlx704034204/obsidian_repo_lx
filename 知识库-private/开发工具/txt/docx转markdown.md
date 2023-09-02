Writage最新版已收费，这个是可用的老版本：

Writage(Markdown插件) V1.1 官方版 http://www.downxia.com/downinfo/127766.html

文件名：Writage-1.10.msi

# 方法一：Writage + Pandoc 推荐

https://zhuanlan.zhihu.com/p/30891168

https://blog.csdn.net/m0_51607907/article/details/124600475

https://blog.csdn.net/qq15035899256/article/details/125547483

## 下载并安装 Writage，

下载地址：http://www.writage.com/
打开 http://www.writage.com/，点击Download，再点击Download Now完成下载

- 运行安装程序，一般按照默认选项安装就好啦

- 重启电脑，新建或打开任一 `Word` 文档，在 `文件` 菜单栏下选 `另存为`，查看 **【保存类型】** 中是否有 `Markdown` 格式。

  （如果插件安装成功，就会自动出现`Markdown`选项；否则，重新安装一遍吧~）

​		查看效果：

​			我们可以看到的格式可能有些乱，和之前在word格式下的样式不一样。那我们可以通过与Pandoc结合，可以尽可能保留样式。

​			Pandoc是由John MacFarlane开发的标记语言转换工具，可实现不同标记语言间的格式转换，堪称该领域中的“瑞士军刀”。

## 下载安装Pandoc

官方下载地址: 

​	https://pandoc.org/installing.html

​	https://github.com/jgm/pandoc/releases  

​	下载 pandoc-2.19.2-windows-x86_64.zip，然后解压下载的文件，并把路径添加到windows环境变量中，以管理员权限 执行 pandoc -v

运行安装程序，一般按照默认选项安装就好啦

## 再次Word 转 Markdown

这样格式就没有那么乱了。

## 总结

（1）由于markdown中的图片无法设置大小，因此在word中排布的图片格式不标准，需要人工调整：
其他格式，如一级、二级标题，项目列表等基本没有问题

（2）将markdown文档上传至码云等平台并提交

# 方法2 直接用pandoc转换

https://blog.csdn.net/sunnygirltest/article/details/127854258 

https://blog.csdn.net/qq_43840665/article/details/113732305

```pandoc java2.docx -o java2.md```



**windows安装pandoc.zip 的环境变量配置好以后，需要以管理员权限 执行 pandoc -v** 

D:\Installed_software\Professional\text\Pandoc\pandoc-3.1.6.2\pandoc.exe