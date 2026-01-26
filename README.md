# iOS-YJOpenSDK 
YJOpenSDK对应release和demo 

# Release 0.5.0

# Release 0.9.0
1. 新增 YJOpenAccountForgotPasswordTask，使用方法见Demo：ResetPasswordViewController
2. 新增 重置密码接口 resetPassword，使用方法见Demo：ResetPasswordViewController
3. 新增 三方登录接口 thirdPartyLogin，使用方法见Demo：LoginViewController

# 注意
1. 如果要使用附带的Demo App，需要使用申请到的app key和app secret，在SceneDelegate的config进行设置
2. 如果要使用UM登录测试，需要在LoginViewController中使用申请到的um key & token

# Release 0.9.2
1. 更新RMPlayer
使用播放器前，需要检查播放器初始化状态，如未初始化，需要调用 YJRMPEngine.getDefault().initialized() 初始化播放器

详情见文档 8.2章节

Demo DeviceListViewController.preparePlayer()

# Release 0.9.3
1. 更新RMPlayer
    a. 适配新的RMPlayer SDK, 2.4.0-rc4, 增加vod es流下载，文件下载相关示例代码 CloudVodViewController.swift
2. 新增账号注销接口 deregister(), 使用方法见Demo：UserController

# Release 0.9.4
1. 新增账号注册并登录接口 registerAndLogin, 使用方法加Demo：RegisterViewController

# Release 0.9.4
1. Accept Language: cn -> zh-CN

# Release 0.9.6
1. 新增AIAssistant

# Release 0.9.7
1. 适配业务组件小智，开放YJVerifyInfo的country
2. demo新增小智的使用接入

# Release 0.9.8
1. 更新rmp版本至2.5.0-rc.7，增加设备摄像头状态通知示例代码  

# Release 0.9.11
1. 更新rmp版本 

# Release 0.9.12
1. 更新SDK至 0.9.12

# Release 0.9.13
1. 更新RMPlayer到v2.6.0-rc.1_release_a4948562_20260109

# Release 0.9.14
1. 更新RMPlayer到v2.6.0-rc.2_release_8400c4f7_20260114

# Release 0.9.15
1. 支持最新iOS26和最新xcode 下获取 WiFi名称

# Release 0.9.16
1. 更新RMPlayer至v2.6.0-rc.4_release_5cfd0acc_20260120

# Release 0.9.18
1. 更新AIAssistant，版本号0.1.7，支持不同xcode版本进行编译运行

参考demo工程，需要设置如下pod脚本，以及将小智依赖的三方库固定版本号，见demo工程的Podfile
```
pod 'YJSAIAssistant', '0.1.6'

# 神眸小智需要依赖的三方组件，版本号需要对应固定
pod 'SpeechEngineToB', '0.0.12'
pod 'TTNetworkManager', '5.2.210.21'
pod 'FSCalendar', '2.8.4'
pod 'MJRefresh', '3.7.9'
pod 'EmptyDataSet-Swift', '5.0.0'
pod 'CocoaMQTT', '2.1.6'
pod 'MqttCocoaAsyncSocket', '1.0.8'
pod 'SnapKit', '5.6.0'
pod 'SwiftMessages', '9.0.6'
pod 'IQKeyboardManagerSwift', '6.5.12'
pod 'Kingfisher', '6.3.1'

 post_install do |installer|
   installer.pods_project.targets.each do |target|
     target.build_configurations.each do |config|
       config.build_settings['IPHONEOS_DEPLOYMENT_TARGET'] = '13.0'
       # 解决SDK的符号丢失问题
       config.build_settings['BUILD_LIBRARY_FOR_DISTRIBUTION'] = 'YES'
       # 解决本次遇到的 Sandbox rsync 报错
       config.build_settings['ENABLE_USER_SCRIPT_SANDBOXING'] = 'NO'
     end
   end
 end
```

2. 更新AIAssistant支持换肤色

见demo工程DeviceListViewController中的示例代码，将主题色设为红色
```
let aitheme = YJSAITheme()
aitheme.primary = .red
aitheme.answer_bg = .red
aitheme.bg_gradient_rightup = .hexIntColor(hexInt: 0xee969c)
aitheme.bg_gradient_middle = .hexIntColor(hexInt: 0xfddddf)
aitheme.bg_gradient_leftbottom = .white
YJSAIAssistantSDK.default.setTheme(aitheme)
```

3. AIAssistant支持我想要气泡能力

# Release 0.9.19
1. 视频通话模式：优化手机camera开关预览速度
