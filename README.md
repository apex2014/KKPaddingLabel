KKPaddingLabel 
===
[![](https://img.shields.io/badge/pod-1.0.1-orange.svg?url=www.baidu.com)](https://cocoapods.org/pods/KKPaddingLabel) [![](https://img.shields.io/badge/platform-ios%20%7C%20osx%20%7C%20watchos%20%7C%20tvos-lightgrey.svg)](https://cocoapods.org/pods/KKPaddingLabel) [![](https://img.shields.io/badge/blog-简书-E87040.svg)](https://www.jianshu.com/p/57776de0a507)


#### 可以给Label添加内边距，支持xib可视化修改，支持autolayout/masonry约束
#### xib效果 动图
-------
![xib可视化编辑内边距](https://github.com/cocoZ/photos/blob/master/KKPaddingLabel2.mov.gif?raw=true "示例图")

#### 代码效果-灰色背景的Label（见下图）, Masonry约束效果相同 
-------
    KKPaddingLabel *paddingLabel = [[KKPaddingLabel alloc] initWithFrame:CGRectZero];
    paddingLabel.text = @"KKPaddingLabel";
    paddingLabel.backgroundColor = [UIColor lightGrayColor];
    paddingLabel.padding = UIEdgeInsetsMake(10, 10, 10, 10);
    paddingLabel.cornerRadius = 5.0f;
    paddingLabel.translatesAutoresizingMaskIntoConstraints = NO;
    [self.view addSubview:paddingLabel];
    
    [self.view addConstraint:[NSLayoutConstraint constraintWithItem:paddingLabel attribute:NSLayoutAttributeTop relatedBy:NSLayoutRelationEqual toItem:self.view attribute:NSLayoutAttributeTop multiplier:1.0 constant:200.0f]];
    [self.view addConstraint:[NSLayoutConstraint constraintWithItem:paddingLabel attribute:NSLayoutAttributeLeft relatedBy:NSLayoutRelationEqual toItem:self.view attribute:NSLayoutAttributeLeft multiplier:1.0 constant:100.0f]];

![Image text](https://github.com/cocoZ/photos/blob/master/WX20181226-161216@2x.png?raw=true "示例图")
