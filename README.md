## 说明
野火IM系统有4部分组成，服务器部分/[iOS](https://github.com/wildfirechat/ios-chat)部分/[Android](https://github.com/wildfirechat/android-chat)部分/协议栈部分（mars）。其中iso和android都依赖于协议栈部分。此为协议栈工程。


### iOS的编译

在${mars}/mars/libraries/目录下执行下面命令，然后copy生成的```mars.framework```到```ios-workspace/wfchatclient/Framework```目录下
```
python build_apple.py
```

### Android的编译
在${mars}/mars/libraries/目录下执行
```
python build_android.py
```

等待编译完成后，在进入到${mars}/mars/libraries/mars_android_sdk目录下执行
```
./gradlew build
```

编译完成后就能在build/output/aar目录下得到mars-core-release.aar, copy到```android-chat/mars-core-release```目录下

#### 鸣谢
1. [mars](https://github.com/Tencent/mars) 作为本项目的基础
2. [pbc](https://github.com/cloudwu/pbc) 提供序列化能力
3. [libemqtt](https://github.com/menudoproblema/libemqtt) 提供mqtt协议处理能力
4. [wcdb](https://github.com/Tencent/wcdb) 提供了协议层使用数据库私聊
5. [sqlcipher](https://github.com/sqlcipher/sqlcipher) 提供了数据库加密能力

***对以上项目的作者衷心的感谢，世界因你们的分享变得更美好。***

## License

Under the MIT license. See the [LICENSE](https://github.com/wildfirechat/mars/blob/firechat/LICENSE) file for details.
