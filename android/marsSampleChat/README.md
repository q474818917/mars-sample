## mars-android
该 demo 的界面借鉴于 weidi1989 的博客中 [Android 之高仿微信聊天的界面](http://blog.csdn.net/way_ping_li/article/details/8008435)。

## 启动
修改替换云服务域名marsopen.cn的NewDNS解析(MarsServiceStub.java)：
```
{
    @Override
    public String[] onNewDns(String host) {
        return new String[]{
                "118.89.24.72"
        };
    }
}
```
将"118.89.24.72"替换为"127.0.0.1"，并且需要将app/build.gradle里的useLocalMarsWrapper修改为true，使用本地wrapper project

## QA
+ ERROR: Failed to resolve: com.android.support:appcompat
解决办法：将app下的build.gradle增加
```
repositories {
    maven {
        url "https://maven.google.com"
    }
}
```
