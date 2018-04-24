# EBCountDownButton
Countdown button for iOS


# 效果图

![](https://upload-images.jianshu.io/upload_images/2107229-addf851d643d8cd7.gif?imageMogr2/auto-orient/strip%7CimageView2/2/w/360)

> 效果图上由于转成gif图之后帧率切换很快啊，实际上是一秒一秒的计时的。



# 调用方式

```
    EBCountDownButton *countDownButton = [[EBCountDownButton alloc] initWithFrame:CGRectMake(100, 100, 140, 40)];
    [countDownButton setTitle:@"获取验证码" forState:UIControlStateNormal];
    [countDownButton setTitleColor:[UIColor whiteColor] forState:UIControlStateNormal];
    countDownButton.backgroundColor = [UIColor colorWithRed:40/255.0 green:207/255.0 blue:155/255.0 alpha:1];
    [countDownButton addTarget:self action:@selector(sendVerificationCode:) forControlEvents:UIControlEventTouchUpInside];
    [self.view addSubview:countDownButton];
```

```
- (void)sendVerificationCode:(EBCountDownButton*)countDownButton {
    [countDownButton countDownWithDuration:5 completion:^(BOOL finished) {
        NSLog(@"finished");
    }];
}
```


[博客地址:https://www.jianshu.com/p/8fc08e9ba283](https://www.jianshu.com/p/8fc08e9ba283)
