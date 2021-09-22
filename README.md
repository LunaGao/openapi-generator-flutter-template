# openapi-generator-flutter-template

基于 [openapi-generator](https://openapi-generator.tech/) [dart](https://openapi-generator.tech/docs/generators/dart) 模板修改而来。
支持Flutter nullsafe。 相当于生成了一个[第三方的库](https://flutter.dev/docs/development/packages-and-plugins/developing-packages)，来帮助访问api。

## 如何使用：
* 直接下载本项目源码
* 仍然使用`openapi-generator`命令

我是在macOS下使用brew安装的，所以命令直接为`openapi-generator`
```
openapi-generator generate -g dart -t TEMPLATE_PATH -o OUT_PUT_PATH -i JSON_FILE
cd OUT_PUT_PATH
flutter pub get
```
命令说明：
```
openapi-generator generate
    -g dart #<-- [1]
    -t TEMPLATE_PATH #<-- [2]
    -o OUT_PUT_PATH #<-- [3]
    -i JSON_FILE #<-- [4]
cd OUT_PUT_PATH #<-- [5]
flutter pub get #<-- [6]
```
* [1] : 这行必须有，这里是指定使用dart来进行生成
* [2] : 这里就是本项目的 `template` 文件夹的目录，可以是绝对路径，也可以是相对路径
* [3] : 生成的api文件夹路径，可以是绝对路径，也可以是相对路径
* [4] : 这里是openapi的json文件，可以是本地文件路径，也可以是网络地址
* [5] : 切换到生成文件的目录
* [6] : 使用命令获取依赖包（这里是flutter的知识，若不明白请查询[flutter](https://flutter.dev/docs/development/packages-and-plugins/developing-packages)）

## 其他
* 修改包名：`--additional-properties=pubName=PUB_NAME`
```
openapi-generator generate -g dart -t template -o api -i openapi.json --additional-properties=pubName=generated-api
```


## 已知问题
* 生成的包中，很大概率 `test` 文件夹内会有文件报错。若您介意可以手动修改或尝试修改模板文件。若不介意可直接删掉，不影响。