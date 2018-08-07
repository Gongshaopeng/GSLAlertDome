# GSLAlertDome

#### 项目介绍
自定义弹窗，虽然同样的Dome很多，但我还是厚颜无耻的再共享一个自己写的吧！这个弹窗我定义了两种实现模式，一种是 alloc 创建对象，另一种就是 单利防止重复弹出，其实dome 不是重要的，重要的是思路，希望对路过的你有帮助。


+ 方法一：
```
GSLAlertView * alertGs = [[GSLAlertView alloc] initWithTitle:@"提示" message:@"获取天气失败！\n解决办法：\n1.手动选择地区 \n2.敬请等待其服务地区信息更新" sureBtn:@"知道了" cancleBtn:nil];
alertGs.resultIndex = ^(NSInteger index) {

};
[alertGs showGSAlertView];
```
+ 方法二
```
[[GSLAlertView alertManager] createInitWithTitle:@"相机授权,才可开启美颜相机哟！" message:@"跳转相机授权设置" sureBtn:@"设置" cancleBtn:@"取消"];
[GSLAlertView alertManager].resultIndex = ^(NSInteger index) {
if (index == 2) {

}else{

}
};
[[GSLAlertView alertManager] showGSAlertView];
```

