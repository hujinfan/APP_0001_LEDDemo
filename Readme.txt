0.git init (第一次执行即可)
1.git add -A
2.git commit -m "v1, created by android studio"
3.git tag v1
4.git remote add origin https://github.com/hujinfan/APP_0001_LEDDemo （第一次执行即可）
5.git push -u origin master
6.git push origin --tags

下载代码：
第一次：
git clone https://github.com/hujinfan/APP_0001_LEDDemo.git

以下命令要在APP_0001_LEDDemo目录里执行：

更新本地代码：
git pull origin

取出指定版本：
git checkout v1
...

添加了button，checkbox
1.git add -A
2.git commit -m "v2,add button and checkbox"
3.git tag v2
4.git push origin master
5.git push origin --tags

添加了button, checkbox的点击方法
1.git add -A
2.git commit -m "v3,add methods for button and checkbox"
3.git tag v3
4.git push origin master
5.git push origin --tags

实现接口方法：Ctrl+I
智能分析表达式，列出可能要写的方法名、变量名：Ctrl+Shift+空格  （强制转换）

add jni
1.git add -A
2.git commit -m "v4,add jni"
3.git tag v4
4.git push origin master
5.git push origin --tags

捕获异常快捷键：Ctrl+Alt+T
1.编译出来的库文件放在：APP_0001_LEDDemo/app/libs/armeabi(自己创建)目录下；
2.修改build.gradle(Module:app),加上：(文件位于:APP_0001_LEDDemo/app/build.gradle)
sourceSets {
        main {
            jniLibs.srcDirs = ['libs']
        }
    }
编译出来的app程序位于：APP_0001_LEDDemo\app\build\outputs\apk\app-debug.apk


调用了ledOpen, ledCtrl
1.git add -A
2.git commit -m "v5,call ledOpen() and ledCtrl()"
3.git tag v5
4.git push origin master
5.git push origin --tags

跳到定义的位置：Ctrl+B



使用硬件访问服务
use ILedService to access led
1.git add -A
2.git commit -m "v6, use ILedService to access led"
3.git tag v6
4.git push origin master
5.git push origin --tags

Ctrl+R 替换
删掉hardlibrary文件夹：APP_0001_LEDDemo\app\src\main\java\com\hujinfan\hardlibrary

识别不出外部类
1.将编译出来的classes.jar复制出来
out/target/common/obj/JAVA_LIBRARIES/framework_intermediates/classes.jar
2.在Android Studio中进行包含
2.1 Ctrl+Alt+Shift+S （project structure ）





a. 包含什么
out/target/common/obj/JAVA_LIBRARIES/framework_intermediates/classes.jar

How do I build the Android SDK with hidden and internal APIs available?
http://stackoverflow.com/questions/7888191/how-do-i-build-the-android-sdk-with-hidden-and-internal-apis-available

b. 怎么包含
Creating a module library and adding it to module dependencies
https://www.jetbrains.com/idea/help/configuring-module-dependencies-and-libraries.html

编译错误
a. java.lang.OutOfMemoryError: GC overhead limit exceeded

Android Studio Google jar causing GC overhead limit exceeded error
http://stackoverflow.com/questions/25013638/android-studio-google-jar-causing-gc-overhead-limit-exceeded-error

修改build.gradle(Module:app),加上：(文件位于:APP_0001_LEDDemo/app/build.gradle)
dexOptions {
        javaMaxHeapSize "4g"
    }

b. Too many field references

Building Apps with Over 65K Methods
https://developer.android.com/tools/building/multidex.html
1.修改build.gradle(Module:app),加上：(文件位于于:APP_0位1_LEDDemo/app/build.gradle)添加如下代码：
defaultConfig{
	.....
	// Enabling multidex support.
        multiDexEnabled true
	......
}

dependencies {
	compile 'com.android.support:multidex:1.0.0'
}

2.修改文件：APP_0001_LEDDemo\app\src\main\AndroidManifest.xml
<application
	.........
	android:name="android.support.multidex.MultiDexApplication"
	.........
</application>
