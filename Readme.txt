0.git init (��һ��ִ�м���)
1.git add -A
2.git commit -m "v1, created by android studio"
3.git tag v1
4.git remote add origin https://github.com/hujinfan/APP_0001_LEDDemo ����һ��ִ�м��ɣ�
5.git push -u origin master
6.git push origin --tags

���ش��룺
��һ�Σ�
git clone https://github.com/hujinfan/APP_0001_LEDDemo.git

��������Ҫ��APP_0001_LEDDemoĿ¼��ִ�У�

���±��ش��룺
git pull origin

ȡ��ָ���汾��
git checkout v1
...

�����button��checkbox
1.git add -A
2.git commit -m "v2,add button and checkbox"
3.git tag v2
4.git push origin master
5.git push origin --tags

�����button, checkbox�ĵ������
1.git add -A
2.git commit -m "v3,add methods for button and checkbox"
3.git tag v3
4.git push origin master
5.git push origin --tags

ʵ�ֽӿڷ�����Ctrl+I
���ܷ������ʽ���г�����Ҫд�ķ���������������Ctrl+Shift+�ո�  ��ǿ��ת����

add jni
1.git add -A
2.git commit -m "v4,add jni"
3.git tag v4
4.git push origin master
5.git push origin --tags

�����쳣��ݼ���Ctrl+Alt+T
1.��������Ŀ��ļ����ڣ�APP_0001_LEDDemo/app/libs/armeabi(�Լ�����)Ŀ¼�£�
2.�޸�build.gradle(Module:app),���ϣ�(�ļ�λ��:APP_0001_LEDDemo/app/build.gradle)
sourceSets {
        main {
            jniLibs.srcDirs = ['libs']
        }
    }
���������app����λ�ڣ�APP_0001_LEDDemo\app\build\outputs\apk\app-debug.apk


������ledOpen, ledCtrl
1.git add -A
2.git commit -m "v5,call ledOpen() and ledCtrl()"
3.git tag v5
4.git push origin master
5.git push origin --tags

���������λ�ã�Ctrl+B



ʹ��Ӳ�����ʷ���
use ILedService to access led
1.git add -A
2.git commit -m "v6, use ILedService to access led"
3.git tag v6
4.git push origin master
5.git push origin --tags

Ctrl+R �滻
ɾ��hardlibrary�ļ��У�APP_0001_LEDDemo\app\src\main\java\com\hujinfan\hardlibrary

ʶ�𲻳��ⲿ��
1.�����������classes.jar���Ƴ���
out/target/common/obj/JAVA_LIBRARIES/framework_intermediates/classes.jar
2.��Android Studio�н��а���
2.1 Ctrl+Alt+Shift+S ��project structure ��





a. ����ʲô
out/target/common/obj/JAVA_LIBRARIES/framework_intermediates/classes.jar

How do I build the Android SDK with hidden and internal APIs available?
http://stackoverflow.com/questions/7888191/how-do-i-build-the-android-sdk-with-hidden-and-internal-apis-available

b. ��ô����
Creating a module library and adding it to module dependencies
https://www.jetbrains.com/idea/help/configuring-module-dependencies-and-libraries.html

�������
a. java.lang.OutOfMemoryError: GC overhead limit exceeded

Android Studio Google jar causing GC overhead limit exceeded error
http://stackoverflow.com/questions/25013638/android-studio-google-jar-causing-gc-overhead-limit-exceeded-error

�޸�build.gradle(Module:app),���ϣ�(�ļ�λ��:APP_0001_LEDDemo/app/build.gradle)
dexOptions {
        javaMaxHeapSize "4g"
    }

b. Too many field references

Building Apps with Over 65K Methods
https://developer.android.com/tools/building/multidex.html
1.�޸�build.gradle(Module:app),���ϣ�(�ļ�λ����:APP_0λ1_LEDDemo/app/build.gradle)������´��룺
defaultConfig{
	.....
	// Enabling multidex support.
        multiDexEnabled true
	......
}

dependencies {
	compile 'com.android.support:multidex:1.0.0'
}

2.�޸��ļ���APP_0001_LEDDemo\app\src\main\AndroidManifest.xml
<application
	.........
	android:name="android.support.multidex.MultiDexApplication"
	.........
</application>
