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

