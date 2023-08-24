uni-app项目没有被HBuilde编译就直接导入到微信小程序工具中辉报错：
	[ app.json 文件内容错误] app.json: 在项目根目录未找到
	原因：
		uni-app 项目 还未转成微信小程序 需要转换一下；
		重点:   首先一定要有 unpackage文件夹   如果没有的需要到HBuilder X 编译一下

编译之前 要在微信小程序开启端口号   设置  -  安全设置 - 安全 - 打开 服务端口；
把项目导入到HBuilder ，点击：运行(运行时压缩代码)-> 运行到小程序模拟器-> 微信开发者工具;
在微信开发者工具中点击：
	详情-本地设置-勾选不校验合法域名...
	   -基本信息-填入个人的APPID

git clone --branch dev-lx https://gitee.com/space704034204/mall-app-web-macrozheng

注意：
	后端的接口地址修改的位置： utils - requestUtil.js
	config.baseUrl = 'http://localhost:8085'
	替换为自己的后台接口地址即可运行
仅供参考：
	https://blog.csdn.net/m0_47890251/article/details/119654609
	https://blog.csdn.net/qq_36174081/article/details/111714777