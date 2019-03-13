#### **RN项目**

xcode升级到10之后，iOS遇到的坑，总结：

1、'config.h' file not found

解决方法：

```
cd node_modules/react-native/third-party/glog-0.3.4
../../scripts/ios-configure-glog.sh
```

如果上面的不行，直接重新init一遍react-native : [https://reactnative.cn/docs/0.42/upgrading.html\#content](https://reactnative.cn/docs/0.42/upgrading.html#content)

然后再使用上面的命令。  
2、'React/RCTBridgeModule.h' / 'RCTBridgeModule.h' file not found

解决解决：

上面的文件在React工程理，在选择工程项目的地方加上加上React,先编译一下React,React编译通过了，再去运行原来项目。

3、Build input file cannot be found: '/xxxt/libfishhook.a'

解决方法：![](/assets/2470023-f4ca8dd2b8a811bb.jpg)4、Build input file cannot be found:'xxx/node\_modules/@0x5e/react-native-alipay/ios/libAlipaySDK.a

解决方法：

在RCTAlipay工程，Link Binary With Libraries中找到AlipaySDK,并去掉它，然后如下图，从此路径选择libAlipaySDK.a即可  
![](/assets/import.png)

