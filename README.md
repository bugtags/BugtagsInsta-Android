# BugtagsInsta Android SDK

[ ![Download](https://api.bintray.com/packages/bugtags/maven/bugtags-insta/images/download.svg) ](https://bintray.com/bugtags/maven/bugtags-insta/_latestVersion)

BugtagsInsta for Android, a powerful plugin for [Bugtags SDK](https://github.com/bugtags/Bugtags-Android)， monitor your mobile app in real-time, providing instant & rich information for your development.

# Features
1. Real-time monitor cpu, memory & storge usage.
2. Real-time monitor console logs.
3. Real-time monitor user operate steps.
4. Real-time monitor network reqeust data.

Learn more: https://docs.bugtags.com/zh/bugtagsinsta/index.html

## Requirements

BugtagsInsta requires SDK 9 and above.

### Integration Steps(Android Studio)
1.Setup dependency in your app module's build.gradle

```
dependencies {
	...
	    
    compile 'com.bugtags.library:bugtags-insta:latest.integration'
}
```

sync gradle file, library will be downloaded in seconds.

2.After start Bugtags SDK, register BugtagsInsta as a plugin

```
Bugtags.start("APP_KEY", this, Bugtags.BTGInvocationEventBubble);
Bugtags.registerPlugin(new BugtagsInsta());
```

3.You can customized listening port(10222 by default) of `BugtagsInsta` by passing an constructor parameter(it's recommended to be greater than 10000)：

```
Bugtags.start("APP_KEY", this, Bugtags.BTGInvocationEventBubble);
Bugtags.registerPlugin(new BugtagsInsta(10080));
   
```

### Integration Steps(Eclipse)

1. Download [SDK](http://bugtags.io/url/bugtagsinsta-android) and extract it

2. drag `bugtags-insta-[version].jar` to libs folder of Eclipse, and add to buildpath

3. After start Bugtags SDK, register BugtagsInsta as a plugin

    ```
    Bugtags.start("APP_KEY", this, Bugtags.BTGInvocationEventBubble);
    Bugtags.registerPlugin(new BugtagsInsta());
    ```

4. You can customize listening port(10222 by default) of `BugtagsInsta` by passing an constructor parameter(it's recommended to be greater than 10000)：

    ```
    Bugtags.start("APP_KEY", this, Bugtags.BTGInvocationEventBubble);
    Bugtags.registerPlugin(new BugtagsInsta(10080));
    
    ```