# iOS9&Xcode7爬坑记
- error:does not contain bitcode. You must rebuild it with bitcode enabled-xcode7
	- http://stackoverflow.com/questions/30848208/new-warnings-in-ios9
	- You library was compiled without bitcode but the bitcode option is enabled in your project settings. Say NO to Enable Bitcode in your target Build Settings and the Library Build Settings to remove the warnings.

- Assertion failure in -[UIApplication 	- xcode
	- _runWithMainScene:transitionContext:completion:], /BuildRoot/Library/Caches/com.apple.xbs/Sources/UIKit_Sim/UIKit-3512.29.5/UIApplication.m:3299
	
- The resource could not be loaded because the App Transport Security policy requires the use of a secure connection.
	- http://segmentfault.com/a/1190000002933776
	- 新特性要求App内访问的网络必须使用HTTPS协议。
但是现在公司的项目使用的是HTTP协议，使用私有加密方式保证数据安全。现在也不能马上改成HTTPS协议传输。
	- 解决方案
		- 在Info.plist中添加NSAppTransportSecurity类型Dictionary。
		- 在NSAppTransportSecurity下添加NSAllowsArbitraryLoads类型Boolean,值设为YES
- iOS9友盟分享
	- 
