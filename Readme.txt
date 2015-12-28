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