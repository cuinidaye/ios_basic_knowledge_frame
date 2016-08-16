# iOS App 发布流程

1.	修改 app 内“关于我们”页面的版本号
	*	“我的” -> “设置” -> “关于我们”
2.	修改项目的版本号和 Build 号
	*	工程项目 -> Targets -> General -> Identity -> Version 和 Build
	*	关于 Build 号:
	```
	git log | grep -e 'commit [a-zA-Z0-9]*' | wc -l
	```
3.	使用发布证书
	*	工程项目 -> Targets -> Build Settings -> Code Signing -> Code Signing Identity 和 Provisioning Profile
4.	选择运行设备
	*	运行设备不能是模拟器
5.	`Edit Scheme` -> `Archive` -> `Build Configuration` 改为 `Release`
6.	Product -> Archive -> UploadToAppStore
