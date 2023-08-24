



Typora编辑区域空白过大问题 https://blog.csdn.net/qq_41489540/article/details/118337976 

## 问题所在

笔记本电脑全屏模式下,[typora](https://so.csdn.net/so/search?q=typora&spm=1001.2101.3001.7020)软件两边留白太大了,感觉中间可以显示的内容太少了…

![在这里插入图片描述](https://img-blog.csdnimg.cn/20210629161751692.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3FxXzQxNDg5NTQw,size_16,color_FFFFFF,t_70)

## 解决办法

## 查看自己用的主题

![在这里插入图片描述](https://img-blog.csdnimg.cn/20210629161843803.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3FxXzQxNDg5NTQw,size_16,color_FFFFFF,t_70)  
发现是[Github](https://so.csdn.net/so/search?q=Github&spm=1001.2101.3001.7020)主题,先记录下来

## 打开偏好设置里面的主题文件

![在这里插入图片描述](https://img-blog.csdnimg.cn/20210629161925461.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3FxXzQxNDg5NTQw,size_16,color_FFFFFF,t_70)

![在这里插入图片描述](https://img-blog.csdnimg.cn/20210629161941187.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3FxXzQxNDg5NTQw,size_16,color_FFFFFF,t_70)

## 编辑主题文件

![在这里插入图片描述](https://img-blog.csdnimg.cn/20210629162018682.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3FxXzQxNDg5NTQw,size_16,color_FFFFFF,t_70)  
我是github主题,所有就编辑github.css主题文件,编辑之前别忘了备份一下

编辑:

编辑文件的max-width

```
#write {
    max-width: 1920px;
  margin: 0 auto;
  padding: 30px;
    padding-bottom: 100px;
}

@media only screen and (min-width: 1400px) {
#write {
max-width: 1920px;
}
}

@media only screen and (min-width: 1800px) {
#write {
max-width: 1920px;
}
}
```

## 查看效果

关闭所有的typora程序,然后重新用typora打开markdown文件,你会发现留白都没了…

![在这里插入图片描述](https://img-blog.csdnimg.cn/20210629162444283.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3FxXzQxNDg5NTQw,size_16,color_FFFFFF,t_70)