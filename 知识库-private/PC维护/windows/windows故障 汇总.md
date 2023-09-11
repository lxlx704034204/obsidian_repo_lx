

### 应用程序驱动版本问题
现象：打开剪影应用程序，windows会100%卡死失去响应，接着蓝屏重启。
检测工具：
	blueScreenView.exe，发现蓝屏次数一小时就有五六次，都指向一个驱动文件dxgkrnl.sys ，度娘发现与显卡有关；
	然后用显卡甜甜圈检测显卡没有发现异常信息(20min)。
查看电脑显卡配置：
	发现一个**独立显卡**：intel® iris® Xe MAX 100 Graphics  锐距系列显卡 性能相当于GTX1030；
	电脑桌面应该是联想出厂预装的一个win11家庭版系统，包括所有的驱动
决定重装系统，备份文件
	重装之后 把客户桌面上的软件快捷方式有拷贝回去之后，用blueScreenView.exe检测，或打开剪影发现还是照样蓝屏，跟上次蓝屏一模一样。
	接着进行检测：尝试把显卡的驱动禁用掉(intel(R) UHD Discrete Graphics)之后，打开剪影发现就不会蓝屏了！ 
		intel® UHD Discrete Graphics   Intel处理器**核显**
		intel® UHD Graphics            Intel处理器**核显**
		intel® Iris® Xe Graphics       Intel处理器**核显** 英特尔锐炬® Xe 显卡。
最终决定到intel官网更新显卡驱动，下载最新版本，安装完成打开剪影发现无蓝屏，重启电脑打开剪影发现无蓝屏。