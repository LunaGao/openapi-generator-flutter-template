# openapi-generator-flutter-template

基于 [openapi-generator](https://openapi-generator.tech/) [dart](https://openapi-generator.tech/docs/generators/dart) 模板修改而来。
支持Flutter nullsafe。

## 如何使用：
* 直接下载本项目源码
* 仍然使用`openapi-generator`命令

我是在macOS下使用brew安装的，所以命令直接为`openapi-generator`
```
openapi-generator generate -g dart -t out -o api -i openapi.json
```
命令说明：
```
openapi-generator generate
    -g dart #<-- [1]
    -t template #<-- [2]
    -o api #<-- [3]
    -i openapi.json #<-- [4]
```
* [1] : 这行必须有，这里是指定使用dart来进行生成
* [2] : 这里就是本项目的template文件夹的目录，可以是绝对路径，也可以是相对路径
* [3] : 生成的api文件夹路径，可以是绝对路径，也可以是相对路径
* [4] : 这里是openapi的json文件，可以是本地文件路径，也可以是网络地址
