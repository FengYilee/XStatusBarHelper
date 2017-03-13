# XStatusBarHelper
沉浸式状态栏工具类
![效果图](https://github.com/fodroid/XStatusBarHelper/blob/master/capture/device-2017-02-21-224549545.png)

#Usage 使用

`gradle`

Add it in your root build.gradle at the end of repositories:

    allprojects {
        repositories {
            ...
            maven { url 'https://jitpack.io' }
        }
    }
Add the dependency

    dependencies {
        compile 'com.github.fodroid:XStatusBarHelper:v1.1'
    }
`maven`

    <repositories>
        <repository>
            <id>jitpack.io</id>
            <url>https://jitpack.io</url>
        </repository>
    </repositories>

    <dependency>
        <groupId>com.github.fodroid</groupId>
        <artifactId>XStatusBarHelper</artifactId>
        <version>v1.1</version>
    </dependency>

###具体调用
`包含DrawerLayout`

    XStatusBarHelper.tintStatusBarForDrawer(this, drawer, getResources().getColor(R.color.colorPrimary));

`效果一`

    XStatusBarHelper.tintStatusBar(this, getResources().getColor(R.color.colorPrimary));
    //或者采用一下方式
    Toolbar toolbar = (Toolbar) findViewById(R.id.toolbar);
    XStatusBarHelper.forceFitsSystemWindows(this);
    XStatusBarHelper.immersiveStatusBar(this);
    XStatusBarHelper.setHeightAndPadding(this, toolbar);

`效果二`

    Toolbar toolbar = (Toolbar) findViewById(R.id.toolbar);
    XStatusBarHelper.forceFitsSystemWindows(this);
    XStatusBarHelper.immersiveStatusBar(this);
    XStatusBarHelper.setHeightAndPadding(this, toolbar);

详细的调用方式，可以查看/app/src/main/java/me/shihao/xstatusbarhelper

## 相关文章

[如何实现沉浸式状态栏](http://www.jianshu.com/p/00fed1371bb0)

#### 如果你觉得有用，请不吝star
