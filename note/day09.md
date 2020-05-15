## 今日任务
    1). 注册
    2). 登陆
    3). 自动登陆
    4). 退出登陆 (自己做一下)

## 注册/登陆的路由组件

## 相关的API
    注册
    登陆
    退出登陆

## 注册
    动态显示一次图形验证码, 点击更新图形验证码
    收集用户输入数据: v-model
    进行前台表单验证, 不通过显示提示信息
    发送注册的请求
    如果失败, 提示失败/更新一下图形验证码
    如果成功了, 跳转到登陆的页面

## 登陆
    收集用户输入数据: v-model
    进行前台表单验证, 不通过显示提示信息
    发送登陆的请求
    如果失败, 提示失败
    如果成功了:
        将用户信息(包括token)保存到vuex和localStorage
        跳转到首页  ==> ???后面会优化此功能

## 自动登陆
    方式一: 登陆请求成功后, 将用户的所有信息(用户名/token)保存到localStorage中, 
            初始访问时, 自动读取localStorage中的用户信息来实现自动登陆(不用发请求获取)
    方式二: 登陆请求成功后, 只将用户的token保存到localStorage中
            初始访问时, 自动读取localStorage中的token, 并发送请求根据token获取用户信息(需要发请求获取) 
    注意: 我们的后台没有一个根据token获取用户信息的接口, 只能用方式1

## 退出登陆
    发送退出登陆的请求
    清除用户信息数据(vuex/localStorage)