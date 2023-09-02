https://www.jianshu.com/p/53bc8430481d PicGo + GitHub 搭建个人图床工具
https://zhuanlan.zhihu.com/p/491649092   PicGo + GitHub  图床 
https://zhuanlan.zhihu.com/p/551244004  Obsidian+picogo+github建造个人markdown笔记
https://blog.csdn.net/weixin_52034760/article/details/128715443 PicGo+Github搭建图床
https://zhuanlan.zhihu.com/p/489236769  github+picGo+typora

## Typora主要功能 汇总
Typora Pandoc 文件格式转换导出
https://zhuanlan.zhihu.com/p/639609854 
## 图片问题

### 图片引用格式

本地引用(网络图片无效！)
```
![[Pasted image 20230808104726.png]]
```
网络图片(本地图片有效！)：

```
![s1](https://img-blog.csdnimg.cn/20200822014538211.png)
```





### 调整图片位置

#### 方法1：最前面或最后面输入一个空格

本地、网图：typora中有效，obsidian中无效。

#### 方法2：嵌入 HTML 代码。

**p标签：本地、网图：typora、obsidian中无效 都中有效！**
```
<p><img src="https://img-blog.csdnimg.cn/20200822014538211.png" align="left" width=20%/></p>
```
<p><img src="https://img-blog.csdnimg.cn/20200822014538211.png" align="left" width=20% /></p>

div标签：本地、网图：typora中有效，obsidian中无效。

```
<div align=left><img src=https://img-blog.csdnimg.cn/20200822014538211.png /></div>
```

<div align=left> <img src=https://img-blog.csdnimg.cn/20200822014538211.png /> </div>



#### 方法3：添加位置标识

在 ULR 末尾添加位置标识 pic_left

本地、网图 都没成功过！
```
![s1](https://img-blog.csdnimg.cn/20200822014538211.png#pic_center =30x30)
```
### 调整图片大小

#### 3.1 等比缩放

##### 3.1.1 相对父级元素

使用 img 标签表示图片时采用百分比形式只定义宽即可等比例缩放。注意：宽度相对于图片所在父级窗口。

没有 hight=1% 属性

```
<img src=https://img-blog.csdnimg.cn/20200822014538211.png width=30% />
```

<img src=https://img-blog.csdnimg.cn/20200822014538211.png width=30% />

##### 3.1.2 相对自身

如果您使用的 Markdown 编辑器支持 CSS 样式的话，那么可以使用 CSS zoom 属性对图片相对于自身大小进行等比缩放。遗憾的是大部分 Markdown 编辑器并不支持 CSS 样式，比如 CSDN Markdown。

```
<img src=https://img-blog.csdnimg.cn/20200822014538211.png style="zoom:30%;" />
```

<img src=https://img-blog.csdnimg.cn/20200822014538211.png style="zoom:30%;" />

一个通用可行的办法是指定宽或高的绝对数值进行等比缩放，只指定宽和高中一个。本文的示例图片尺寸为 481*279px，那么设置图片宽度为 240px 或高度为 140px 即可将图片宽高等比缩小为原来的一半。

```
<img src=https://img-blog.csdnimg.cn/20200822014538211.png width=240 height=140 />
```

<img src=https://img-blog.csdnimg.cn/20200822014538211.png width=240 height=140 />

#### 3.2 非等比缩放

##### 3.2.1 CSS 属性

可以利用 CSS 的属性 `transform:scale(x,y)` 和 `transform-origin:left top` 来完成非等比缩放。其中 `transform-origin:left top` 的作用是改变缩放的中心点位置为左上角，而非默认的中心位置。

```
<img src=https://img-blog.csdnimg.cn/20200822014538211.png style="transform:scale(0.8,0.5);transform-origin:left top;" />
```

<img src=https://img-blog.csdnimg.cn/20200822014538211.png style="transform:scale(0.8,0.5);transform-origin:left top;" />

##### 3.2.2 指定宽高（单位像素）

同样的，大部分 Markdown 编辑器并不支持 CSS 属性。不过好在该种操作并不常见，因为可能会导致图片变形。如果一定要宽高按照不同比例进行缩放，那么可以计算好缩放后的宽高像素值，采用下面指定宽高像素值的方式来实现。

```
<img src=https://img-blog.csdnimg.cn/20200822014538211.png width=240 height=140 />
```

<img src=https://img-blog.csdnimg.cn/20200822014538211.png width=240 height=140  />




## gitee图床 不稳定 不推荐
#注意：因gitee添加了外链，导致利用gitee当图床相当不稳定，不建议使用！！
Gitee官方是禁止免费白票 图床的！
## 配置 GitHub

### 新建仓库：
lxlx704034204/oss_img_lx
勾选 Add a README file
这里需要注意：仓库得设置为 Public 。因为后面通过客户端访问算是外部访问，因此无法访问 Private ，这样的话图片传上来之后只能存储不能显示。

### 生成一个token，用于picGo访问github
	 打开setting -> Developer settings -> PersonaL access tokens -> Tokens(classic) -> Generate new token(classic)
Note  随便写
Expiration  No expiration
只然后勾选“repo”权限
点击页面底部的“Generate token”按钮，然后复制保存好你的token

## 安装配置PicGo
https://github.com/Molunerfinn/picgo/releases   比如：PicGo-Setup-2.4.0-beta.0-x64.exe
安装并打开 PicGo（如果尚未安装）。

点击左侧菜单栏上的“图床设置”，选择“GitHub”作为存储服务，点击 加号,填写配置信息：
	仓库名称（Repository）： lxlx704034204/oss_img_lx
	分支名（Branch）：           main ; 默认为 main 或 master，您可以在 GitHub 仓库中查看默认分支名称。
	访问令牌（Token）：您需要在 GitHub 上创建一个访问令牌。请参阅以下说明来获取令牌。
	存储路径（Path）：默认会上传到根目录，指定目录要以/结尾。例如，设置为 /images/ 
	自定义域名（Custom Domain）：此处可选。如果您有自定义域名，可以在此填写，否则请留空。
		https://cdn.jsdelivr.net/gh/lxlx704034204/oss_img_lx@main
		https://cdn.staticaly.com/gh/lxlx704034204/oss_img_lx@main    jsdelivr失效后的替代品

加速访问 自定义域名中的https://github.com/替换成https://cdn.jsdelivr.net/gh/即可 
	自定义域名的作用是，在上传图片后成功后，PicGo会将“自定义域名+上传的图片名”生成的访问链接，
		放到剪切板上​​https://raw.githubusercontent.com/用户名/RepositoryName/分支名，  
	真实的githu图片访问路径：
		https://raw.githubusercontent.com/lxlx704034204/oss_img_lx/main/images/m1.png 
	
	https://cdn.jsdelivr.net/gh/lxlx704034204/oss_img_lx			ok	访问路径：https://cdn.jsdelivr.net/gh/lxlx704034204/oss_img_lx/images/ma1.png
	https://cdn.jsdelivr.net/gh/lxlx704034204/oss_img_lx@main		ok	访问路径：https://cdn.jsdelivr.net/gh/lxlx704034204/oss_img_lx@main/images/s1.png 推荐★
	https://cdn.jsdelivr.net/gh/lxlx704034204/oss_img_lx/main		ok	配置错误，需要更改访问路径才可以：https://cdn.jsdelivr.net/gh/lxlx704034204/oss_img_lx@main/images/s1.png
	https://ghproxy.com/https://github.com/lxlx704034204/oss_img_lx	fail 配置错误，无法访问
	https://github.com/lxlx704034204/oss_img_lx				        fail 配置错误，无法访问
	
	图片访问：
	https://github.com/lxlx704034204/oss_img_lx/blob/main/images/ma1.png?raw=true			fail 有魔法也fail
	https://raw.githubusercontent.com/lxlx704034204/oss_img_lx/main/images/ma1.png		fail 有魔法也fail 	加 https://ghproxy.com/ ok 必须加上分支名称！
	https://raw.githubusercontent.com/lxlx704034204/oss_img_lx/master/images/ma1.png		fail 有魔法也fail	加 https://ghproxy.com/ ok 必须加上分支名称！
	https://raw.githubusercontent.com/lxlx704034204/oss_img_lx/images/ma1.png				fail 有魔法也fail 	加 https://ghproxy.com/ 404: Not Found
	https://raw.githubusercontent.com/lxlx704034204/oss_img_lx/master/main/images/ma1.png	fail 有魔法也fail	加 https://ghproxy.com/ 404: Not Found


## 开始上传测试

点击picGo左侧的上传 菜单，然后在点击 倒三角 选择 你刚刚配置的GitHub的哪个 ‘图床设置’ 配置，就可以上传测试了

## Obsidian设置
设置->第三方插件->关闭安全模式->社区插件市场->搜索Image auto upload Plugin安装->开启插件即可使用
这样粘贴到 Obsidian 中的图片 就会自动上传到 GitHub图床了。

Image auto upload Plugin 关闭剪贴板自动上传
https://zhuanlan.zhihu.com/p/589898453 

个人建议：需要的时候 自打开‘剪贴板自动上传’！
## 拓展

.trash 相关
	设置-文件与链接-删除文件位置

云端上传 PicGo 
	https://github.com/Molunerfinn/PicGo
云端上传、删除 PicList
	https://github.com/Kuingsmile/PicList
	https://github.com/Kuingsmile/PicHoro https://api.gitee.com/kuingsmile/PicList
		 https://pichoro.horosama.com/#/PicHoroDocs/PicHoro