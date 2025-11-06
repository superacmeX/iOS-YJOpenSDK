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