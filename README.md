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
